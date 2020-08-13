---
title: 使用kendo-ui日期选择框限制指定日期不可选
date: 2019-03-18 19:52:47
tags: [前端,web,kendo]
description: kendo-ui日期控件使用
---

---

需求分析:

>1. 限制双休日日期不可选
>2. 假期日不可选
>3. 三个工作日后的日期不可选,工作日需排除双休日和假期日

使用kendo-ui可以完美实现这些要求，但是使用过程中有好多坑，不过参照我下面的写法就没问题，话不多说，直接上代码吧
<!--more-->
---

首先，创建一个输入框用于kendo日期控件初始化日期选择框
``` html
    <input id="date">
```

引入kendo-ui,由于kendo-ui是依赖于jQuery的，所以还得先引入jQuery
``` javascript
    <script src="/js/jquery.min.js"></script>
    <script type="text/javascript" src="/js/kendo.all.min.js"></script>
```

定义假期日数组,这个假期日不是固定的，可以由用户维护，然后通过ajax请求获取，这里为了方便演示将其定义为固定数组

``` javascript
    let Holiday = [new Date("2019-03-18"),new Date("2019-03-19"),new Date("2019-03-20"),new Date("2019-03-21"),new Date("2019-03-22")]
```

初始化十日内的双休日+假期日，这里为什么只选取十日内的双休日呢，因为在未来的三个工作日之内假期日加上双休日基本不会出现十日以上的情况，这个日期集越小性能越好，所以无需定义更多，当然这里可以根据实际情况多定义几天，但强烈不建议定义整年的双休日，一是完全没必要，二是极其影响性能

``` javascript
    getHoliAndWeekendDay: function(){
        //定义10天内所有的日期
        let Days = [new Date(),
                    new Date(new Date().getTime() + 1*24*60*60*1000),
                    new Date(new Date().getTime() + 2*24*60*60*1000),
                    new Date(new Date().getTime() + 3*24*60*60*1000),
                    new Date(new Date().getTime() + 4*24*60*60*1000),
                    new Date(new Date().getTime() + 5*24*60*60*1000),
                    new Date(new Date().getTime() + 6*24*60*60*1000),
                    new Date(new Date().getTime() + 7*24*60*60*1000),
                    new Date(new Date().getTime() + 8*24*60*60*1000),
                    new Date(new Date().getTime() + 9*24*60*60*1000)]

        //定义周末日期数组
        let WeekendDay = []

        //判断日期是否为周末，是的话添加到周末日期数组
        $.each(Days,function(index,item){
            if(item.getDay()==0 || item.getDay()==6){
                WeekendDay.push(item)
            }
        })

        //将周末日期和假期日合并返回
        return WeekendDay.concat(Holiday)
    }

```

定义compareDates方法用于判断日期是否是同一天，只判断年月日是否相同
``` javascript
    compareDates: function(date, dates) {
        for (let i = 0; i < dates.length; i++) {
            if (dates[i].getDate() == date.getDate() &&
                dates[i].getMonth() == date.getMonth() &&
                dates[i].getYear() == date.getYear()) {
                return true
            }
        }
    }
```

获取三个工作日内的最大日期
``` javascript
    getMaxDate: function(){
        //设置最大日期初始值(第3天)
        let MaxDate = new Date(new Date().getTime() + 3*24*60*60*1000)

        //三个工作日日期数组初始值(先假定未来三天内全是工作日)
        let workDays = [new Date(new Date()),new Date(new Date().getTime() + 1*24*60*60*1000),new Date(new Date().getTime() + 2*24*60*60*1000)]

        //获取假期日+周末日期
        let holiDays = getHoliAndWeekendDay()
        for(let i =0;i<workDays.length;i++){
            //判断工作日是否为假期日或者双休日，是的话最大日期加一天
            if(compareDates(workDays[i],holiDays)){
                MaxDate = new Date(MaxDate.getTime() + 24*60*60*1000)
            }
            //循环判断最新的最大日期是否为假期日或者双休日，是的话最大日期再加一天，直到最大日期不是假期日和双休日则跳出循环
            while(compareDates(MaxDate,holiDays)){
                MaxDate = new Date(MaxDate.getTime() + 24*60*60*1000)
            }
        }
        return MaxDate
    }
```

初始化kendo-ui日期控件
``` javascript
    initKendoDateControl: function (target) {
        target.kendoDatePicker({
        format: "dd MMM yyyy",
        parseFormats: ["yyyy-MM-dd"],
        disableDates:function(date){        //配置禁止选择指定日期
            let isHoliDay = false
            let holiDays = getHoliAndWeekendDay()   //假期日+周末日期
            if (date && compareDates(date,holiDays)){
                isHoliDay = true
            }
            return isHoliDay
        },
        max:getMaxDate()        //定义最大可选日期，即第三个工作日为最大日期，第三个工作日后的所有日期不可宣不可见
        })
        .data('kendoDatePicker').enable(true)

        // 失去焦点时判断日期合法性
        target.on('blur', function () {
            $(this).kendoDateCheck()
        })
    }
```

初始化日期输入框
``` javascript
    initKendoDateControl($("#date"))

    //将日期输入框设置成只可点选不可输入
    $("#date").data("kendoDatePicker").element[0].disabled=true
```

 

由于第一次写博客，不太会组织语言，只能尽量多写点注释，代码实测可行，如有不懂之处可与我联系，感谢查阅！

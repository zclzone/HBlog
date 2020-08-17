---
title: JavaScript的几个很实用的数组方法
top: false
categories: 算法
date: 2020-08-17 16:46:36
tags:
---

## JavaScript 的几个很实用的数组方法

### **some 方法**

> some(): 返回一个 Boolean，判断是否有元素符合 func 条件

```javascript
  let arr = [1,2,3,4];
  arr.some(item => item > 1});  //返回结果true
```

### **every 方法**

> every(): 返回一个 Boolean，判断每一个元素是否符合 func 条件

```javascript
let arr = [1, 2, 3, 4]
arr.every((item) => item > 3) //返回结果false
arr.every((item) => item >= 1) //返回结果true
```

### **filter 方法**

> filter(): 返回一个符合 func 条件的元素数组,不改变原来数组

```javascript
  let ages = [23, 28, 25, 32];
  ages.filter(item => item > 25});  //[28,32]
  console.log(ages);    //[23, 28, 25, 32]
```

此方法非常实用，可以用于删除数组的操作，一般删除数组会用 splice 方法，但此方法用起来很麻烦，首先得找到索引，然后再删除，尤其在遍历删除的时候每删除一个元素，后面的元素索引就会错乱，虽然可以从后往前删，但终究麻烦，不过使用 filter 方法就会简单很多

```javascript
let ages = [23, 28, 25, 32]
ages.filter((item) => item > 25) //删除元素不大于25的所有元素
ages.filter((item, index) => index != 2 && index != 3) //删除索引为2和3的元素
```

### **map 方法**

> 返回一个新的 array，数组元素由每一次调用函数产生结果组成

```javascript
let arr = [1, 2, 3, 4, 5, 6]
arr.map((item) => item + 1) //[2,3,4,5,6,7]
```

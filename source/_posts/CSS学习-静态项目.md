---
title: CSS学习-静态项目
date: 2019-03-25 13:53:37
tags: css
---

最近在学css，学着做了一个静态页面，点击<a href="http://zclzone.com/csspro" target="_blank">zclzone.com/csspro</a>查看效果

<!-- more -->

源码如下：
~~~ html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>学成网教育</title>
        <link rel="stylesheet" href="./css/style.css">
    </head>
    <body>
        <!-- 头部 -->
        <header>
            <nav>
                <!-- logo部分 -->
                <div class="logo">
                    <img src="./images/logo_03.png" alt="">
                </div>
                <!-- 导航栏 -->
                <div class="navbar">
                    <ul>
                        <li><a href="#">首页</a></li>
                        <li><a href="#">课程</a></li>
                        <li><a href="#">职业规划</a></li>
                    </ul>
                </div>
                <!-- 个人中心 -->
                <div class="personal">
                        <a href="#">个人中心<img src="./images/ling_06.png" alt=""></a>
                        <a href="#"><img src="./images/tou_03.png" alt="">Ronnie</a>
                    </div>
                <!-- 搜索框 -->
                <div class="search">
                    <input type="text" placeholder="请输入关键字">
                    <input type="submit" value="">
                </div>
            </nav>
        </header>
        <!-- banner -->
        <div class="banner">
            <div class="banner-in container">
                <!-- 左侧导航栏 -->
                <div class="slidebar">
                    <ul>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                        <li><a href="#">前端开发<span>></span></a></li>
                    </ul>
                </div>
                <!-- 小课表 -->
                <dl class="timetable">
                    <dt>我的课程表</dt>
                    <dd>
                        <h4>继续学习 程序语言设计</h4>
                        <p>正在学习-使用对象</p>
                    </dd>
                    <dd>
                        <h4>继续学习 程序语言设计</h4>
                        <p>正在学习-使用对象</p>
                    </dd>
                    <dd>
                        <h4>继续学习 程序语言设计</h4>
                        <p>正在学习-使用对象</p>
                    </dd>
                    <dd>
                        <a href="#">全部课程</a>
                    </dd>
                </dl>
                <ul class="circle">
                    <li class="current"></li>
                    <li></li>
                    <li></li>
                    <li></li>
                    <li></li>
                    <li></li>
                </ul>

            </div>
        </div>
        <!-- 精品推荐 -->
        <div class="recommend container">
            <li><a href="#">精品推荐</a></li>
            <li><a href="#">Jquery</a></li>
            <li><a href="#">javaWeb</a></li>
            <li><a href="#">Spart</a></li>
            <li><a href="#">MySql</a></li>
            <li><a href="#">javaWeb</a></li>
            <li><a href="#">MySql</a></li>
            <li><a href="#">修改兴趣</a></li>
        </div>
        <!-- 精品推荐大模块 -->
        <div class="recom-products container">
            <div class="recom-hd">
                <h4>精品推荐</h4>
                <a href="#">查看全部</a>
            </div>
            <div class="recom-body clearfix">
                <ul>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                    <li><img src="./images/icon1.png" alt="">
                        <h5>Think PHP 5.0 博客系统实战项目演练</h5>
                        <p><span>高级</span>  •  1125人在学习</p>
                    </li>
                </ul>
            </div>
        </div>
        <!-- 页面底部 -->
        <footer>
            <div class="footer-in container">
                <div class="footer-left">
                    <img src="./images/logo-s.png" alt="">
                    <p>学成在线致力于普及中国最好的教育它与中国一流大学和机构合作提供在线课程。<br />
                        © 2017年XTCG Inc.保留所有权利。-沪ICP备15025210号</p>
                    <a href="#">下载APP</a>
                </div>
                <div class="footer-right">
                    <dl>
                        <dt>关于学成网</dt>
                        <dd><a href="#">管理团队</a></dd>
                        <dd><a href="#">工作机会</a></dd>
                        <dd><a href="#">客户服务</a></dd>
                        <dd><a href="#">帮助</a></dd>
                    </dl>
                    <dl>
                        <dt>关于学成网</dt>
                        <dd><a href="#">管理团队</a></dd>
                        <dd><a href="#">工作机会</a></dd>
                        <dd><a href="#">客户服务</a></dd>
                        <dd><a href="#">帮助</a></dd>
                    </dl>
                    <dl>
                        <dt>关于学成网</dt>
                        <dd><a href="#">管理团队</a></dd>
                        <dd><a href="#">工作机会</a></dd>
                        <dd><a href="#">客户服务</a></dd>
                        <dd><a href="#">帮助</a></dd>
                    </dl>
                </div>
            </div>
        </footer>
    </body>
    </html>
~~~

~~~ css
    * {
        margin: 0;
        padding: 0;
    }
    body {
        background-color: #f3f5f7;
        overflow: auto;
    }
    a {
        color: #050505;
        text-decoration: none;
    }
    li {
        list-style: none;
    }
    .clearfix:before, .clearfix:after {   /* 清除浮动 */
        display: table;
        content: "";
    }
    .clearfix:after {
        clear: both;
    }
    .clearfix {
        *zoom: 1;
    }
    input {
        border: 0;
        box-sizing: border-box;
    }
    .container {
        width: 1200px;
        margin: 0 auto;
    }
    header {
        height: 100px;
        overflow: hidden;
    }
    nav {
        width: 1366px;
        height: 42px;
        margin: 26px auto;
    }
    .logo {
        float: left;
    }
    .navbar {
        float: left;
        height: 42px;
        line-height: 42px;
        margin-left: 50px;
    }
    .navbar li {
        float: left;
    }
    .navbar li a {
        padding: 0 10px;
        display: block;
        height: 40px;
    }
    .navbar li a:hover {
        border-bottom: 2px solid #00a4ff;
    }
    .search {
        width: 410px;
        height: 38px;
        border: 1px solid #00a4ff;
        float: right;
    }
    .search input[type=text] {
        width: 360px;
        height: 38px;
        /* padding-left: 20px; */
        text-indent: 20px;
        float: left;
    }
    .search input[type=submit] {
        width: 50px;
        height: 38px;
        background-color: #00a4ff;
        float: left;
        background: #00a4ff url('../images/search_06.png') center no-repeat
    }
    .personal{
        float: right;
        height: 42px;
        line-height: 42px;
        margin: 0 15px 0 35px;
    }
    .personal img {
        margin: 0 10px;
    }

    .banner {
        height: 420px;
        background-color: #1c036c;
    }
    .banner-in {
        height: 420px;
        background: url('../images/banner_03.png') 0 0 no-repeat;
        position: relative;
    }
    .slidebar {
        height: 420px;
        width: 190px;
        background: rgba(0, 0, 0, 0.4);
        float: left;
    }
    .slidebar li a {
        color: #fff;
        font-size: 14px;
        padding: 0 30px;
        display: block;
        line-height: 45px;
    }
    .slidebar li a:hover {
        color: #00a4ff;
    }
    .slidebar a span {
        float: right;
        font-family: Arial;
    }
    .circle {
        width: 180px;
        height: 22px;
        position: absolute;
        bottom: 10px;
        left: 50%;
        margin-left: -90px;
    }
    .circle li {
        float: left;
        width: 12px;
        height: 12px;
        line-height: 12px;
        background-color: rgba(255, 255, 255, 0.4);
        margin: 5px 8px;
        border-radius: 50%;
    }
    .circle li:hover {
        background-color: rgba(255, 255, 255, 0.8);
    }

    .circle .current {
        width: 19px;
        border-radius: 20%;
        background-color: #fff;
    }

    .timetable {
        float: right;
        width: 230px;
        height: 300px;
        background-color: #fff;
        margin-top: 50px;
        border-radius: 10px;
    }
    .timetable dt {
        line-height: 50px;
        background: #9bceea;
        text-align: center;
        font-weight: 700;
        color: #fff;
        letter-spacing: 2px;  /* 字间距 */
        margin-bottom: 5px;
        border-radius: 10px 10px 0 0;
    }
    .timetable dd {
        width: 193px;
        height: 60px;
        margin: 0 auto;
        border-bottom: 1px solid #ccc;
        padding-top: 12px;
        box-sizing: border-box;
    }
    .timetable dd:last-child {
        border: 0;
    }
    .timetable dd h4 {
        font-size: 16px;
        font-weight: normal;
        color: #4e4e4e;
    }
    .timetable dd p {
        font-size: 14px;
        color: #a5a5a5;
    }
    .timetable dd a {
        border: 1px solid #00a4ff;
        display: block;
        line-height: 38px;
        text-align: center;
        color: #00a4ff;
        font-weight: bold;
        border-radius: 5px;
    }
    .timetable dd a:hover {
        background-color: #00a4ff;
        color: #fff;
    }
    .recommend {
        height: 60px;
        background-color: #fff;
        margin-top: 8px;
        box-shadow: 0 2px 2px rgba(0, 0, 0, 0.2);
    }
    .recommend li {
        display: inline;
        line-height: 60px;
        padding: 0 30px;
        border-right: 1px solid #ccc;
    }
    .recommend li:first-child a {
        color: #00a4ff;
    }
    .recommend li a:hover {
        color: #00a4ff;
    }
    .recommend li:last-child {
        border: 0;
        float: right;
        font-size: 14px;
    }
    .recommend li:last-child a {
        color: #00a4ff;
    }
    .recom-products {
        margin-top: 35px;
    }
    .recom-hd {
        height: 40px;
    }
    .recom-hd h4 {
        float: left;
        color: #494949;
    }
    .recom-hd a {
        float: right;
        margin-top: 10px;
        margin-right: 30px;
        font-size: 14px;
        color: #a5a5a5;
    }
    .recom-hd a:hover {
        color: #00a4ff;
    }
    .recom-body ul li {
        width: 228px;
        height: 270px;
        overflow: hidden;
        background-color: #fff;
        box-shadow: 0 4px 5px rgba(0, 0, 0, 0.4);
        float: left;
        margin-right: 15px;
        margin-bottom: 15px;
        box-sizing: border-box;
    }
    .recom-body ul li:hover {
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.8);
    }

    .recom-body ul li:nth-child(5n) {
        margin-right: 0;
    }
    .recom-body li h5,
    .recom-body li p {
        padding: 0 20px 0 24px;
        margin-top: 15px;
    }
    .recom-body li h5 {
        font-weight: normal;
        font-size: 14px;
        line-height: 22px;
    }
    .recom-body li p {
        font-size: 12px;
        color: #a5a5a5;
    }
    .recom-body p span {
        color: #ff7c2d;
    }
    footer {
        height: 270px;
        margin-top: 100px;
    }
    .footer-in {
        padding-top: 30px;
    }
    .footer-left {
        float: left;
    }
    .footer-left p {
        font-size: 12px;
        line-height: 18px;
        color: #999;
    }
    .footer-left a {
        display: block;
        width: 118px;
        line-height: 33px;
        font-size: 16px;
        color: #00a4ff;
        text-align: center;
        border: 1px solid #00a4ff;
        margin-top: 15px;
        border-radius: 5px;
    }
    .footer-left a:hover {
        color: #fff;
        background-color: #00a4ff;
    }
    .footer-right {
        float: right;
        color: #333;
    }
    .footer-right dl {
        float: left;
        width: 225px;
    }
    .footer-right dt {
        font-size: 16px;
        height: 30px;
    }
    .footer-right dd {
        font-size: 12px;
        height: 20px;
    }
    .footer-right dd a:hover {
        text-decoration: underline;
        color: #00a4ff;
    }
~~~

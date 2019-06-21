# 简单的选项卡效果示例

## 先看效果
https://blog.csdn.net/zt_16KK/article/details/93157490
## HTML代码
```
    <div class="option-card">
        <ul>
            <li>
                <a href="#" class="active-card card" onclick="clickCard(this,'page1')">OPTION 1</a>
            </li>
            <li>
                <a href="#" class="card" onclick="clickCard(this,'page2')">OPTION 2</a>
            </li>
        </ul>
        <div id="page1" class="sub-page show-page">
            <h1>OPTION 1</h1>
        </div>
        <div id="page2" class="sub-page">
            <h1>OPTION 2</h1>
        </div>
    </div>
```

## CSS代码
```
        .option-card {
            width: 100%;
            display: block;
        }

        .option-card>ul {
            display: block;
            width: 100%;
            height: 50px;
            list-style: none;
            border-bottom: solid 1px #a0a0a0;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        .option-card>ul>li {
            display: inline-block;
            margin: 0;
        }

        .option-card>ul>li>a {
            display: block;
            text-decoration: none;
            color: #000;
            text-align: center;
            width: 100px;
            border: solid 1px #a0a0a0;
            border-bottom: none;
            margin: 0;
            line-height: 50px;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
            background-color: bisque;
        }

        .active-card {
            background-color: #fff !important;
        }

        .sub-page {
            display: none;
        }

        .show-page {
            display: block !important;
        }
```

## JS代码
```
function clickCard(e, id) {
        var arr = document.getElementsByClassName("card");
        for (var i = 0; i < arr.length; i++) {
            arr[i].classList.remove("active-card");
        }
        e.classList.add("active-card");

        var arr = document.getElementsByClassName("sub-page");
        for (var i = 0; i < arr.length; i++) {
            arr[i].classList.remove("show-page");
        }
        document.getElementById(id).classList.add("show-page");
    }
```
## 博客
https://blog.csdn.net/zt_16KK/article/details/93157490
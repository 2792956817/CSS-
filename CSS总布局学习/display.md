# display与浮动

- 块级元素：独占一行
```html
h1~h6  div  p  列表  <hr> .....
```

- 行级元素：不独占一行
```html
span a img strong .....
```
_行内元素可以被块级元素包含，块级元素不能被行级元素包含_

## display
常用元素|作用
---|---
block|可以让行内元素 变成块级元素
inline|可以让元素变成行级元素
inline-block|也是一个块级元素，但是可以内联合在一行，即行内块状元素类似img
none|可以让元素失效

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .div1{
            width: 100px;
            height: 100px;
            border: 2px solid red;
            display: inline;
        }
        .div2{
            width: 100px;
            height: 100px;
            border: 2px solid red;
            display: inline-block;
        }
        .div3{
            width: 100px;
            height: 100px;
            border: 2px solid red;
            display: none;
        }
        span{
            width: 100px;
            height: 100px;
            border: 2px solid red;
            display: block;
        }
        p{
            width: 150px;
            height: 150px;
            text-align:center;
            line-height: 150px;
            background-color: pink;
            border: 2px dotted black;
        }
    </style>
</head>
<body>
    <div class="div1"> div块元素</div>
    <div class="div2"> div块元素</div>
    <p>
        中间的div失效
        <div class="div3"> div块元素</div>
    </p>
    <span>span行内元素</span>
</body>
</html>
```

## 浮动
- float
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./css/style.css">
</head>
<body>
    <div id="fater">
        <div class="layer01">
            <img width="330px" height="200px" src="https://img1.baidu.com/it/u=1726475353,306474546&fm=253&fmt=auto&app=138&f=JPEG?w=889&h=500" alt="">
        </div>
        <div class="layer02">
            <img width="330px" height="200px" src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fi.img16888.com%2Fupload%2FImages%2F2021%2F04%2F795991617933372.jpg&refer=http%3A%2F%2Fi.img16888.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1665152836&t=f52b70b6e824f015fddbce95c8d95793" alt="">
        </div>
        <div class="layer03">
            <img width="330px" height="200px" src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fbkimg.cdn.bcebos.com%2Fpic%2Ffaf2b2119313b07e1fcfe16101d7912397dd8c6d&refer=http%3A%2F%2Fbkimg.cdn.bcebos.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1665152883&t=7ae4842d6012841a0642e5570c1dcf7a" alt="">
        </div>
        <div class="layer04">
            1984年考入香港TVB舞蹈训练班。1990年代言光阳机车广告在台湾成名 [2] ；
        </div>
    </div>
</body>
</html>
```

```css
div{
    margin: 10px;
    padding: 10px;
}
#fater{
    border: 2px solid black;
}
.layer01{
    border: 2px solid black;
    display: inline-block;
    float: right;
}
.layer02{
    border: 2px solid black;
    display: inline-block;
    float: right;
}
.layer03{
    border: 2px solid black;
    display: inline-block;
    float: right;
}
.layer04{
    border: 2px solid black;
    display: inline-block;
    float: right;
    clear: both;
}
```

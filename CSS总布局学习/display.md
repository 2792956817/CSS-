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
inline-block|也是一个块级元素，但是可以内联合在一行，
即行内块状元素类似img
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

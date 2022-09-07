
# 【CSS盒子美化】

 ## 一、css盒子模型

### 1.1盒子模型的使用
 ```html
<div></div>
```

### 1.2盒子内外边距

![image](https://user-images.githubusercontent.com/109905813/188826566-8ca2683d-cb0e-48ff-8634-acd4c015a757.png)

-一个盒子由（margin）外边距+(border)边框+(padding)内边距+div盒子真实大小

- 外边距margin

属性|作用
--|--
xx%|用于百分比布局
auto|自动左右
XXpx|固定位置

- 边框border
属性|作用
 --|--
border-widt|边框粗细
border-style|边框样式
border-color|边框颜色

border-style设置|使用效果
----|---
none|无边框
solid|实线
dashed|虚线
dottef|点线

**padding内边距上下-左右或上右下左**

```html
        .one{
            width: 200px;
            height: 200px;
            background-color: rgba(68, 67, 67,0.6);
            border: 3px solid red;
            margin: 0 auto;
            /* margin: 上下 左右; */
        }
        .two{
            width: 100px;
            height: 100px;
            border: 3px solid black;
            margin: auto;
            padding: 30px;
            background-color: #fff;
            position: relative; 
        }
        .three{
            background-color: aqua;
            width: 100%;
            height: 100%;
        }
    <div class="one">
        <div class="two">
            <div class="three"></div>
        </div>
    </div>
```




# user-select

## 说明
用于更改用于计算元素的宽度和高度默认的CSS盒子模型，可以使用此属性来模拟不正确支持CSS盒子模型规范的游览器行为。

例如，假如您需要并排放置两个带边框的框，可通过将 box-sizing 设置为 "border-box"。这可令浏览器呈现出带有指定宽度和高度的框，并把边框和内边距放入框中。

## 语法

box-sizing: content-box|border-box|inherit;

默认值: 	content-box

## 取值

content-box: border和padding不计算入width之内。

border-box: border和padding计算入width之内。

inherit: 规定应从父元素继承 box-sizing 属性的值

## 实例
```HTML
<style type="text/css">
    .content-box{
        box-sizing:content-box;
        -moz-box-sizing:content-box;
        width: 100px;
        height: 100px;
        padding: 20px;
        border: 5px solid #E6A43F;
        background: blue;
    }
    .border-box{
        box-sizing:border-box;
        -moz-box-sizing:border-box;
        width: 100px;
        height: 100px;
        padding: 20px;
        border: 5px solid #3DA3EF;
        background: yellow;
    }
</style>
```

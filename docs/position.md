# position

## 说明
指定一个元素（静态的，相对的，绝对或固定）的定位方法的类型。

## 语法

position: static | fixed | absolute | relative

默认值: text

## 取值

**static**: 默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。

**absolute**: 当Position属性值为absolute时对象从文档流中抽取出来，原占有的位置被后面的对象顶替上来Top的值表示对象上边框与浏览器窗口顶部的距离bottom的值表示对象下边框与浏览器窗口底部的距离两者同时存在时，只有Top起作用；如果两者都未指定，则其顶端将与原文档流位置一致，即垂直保持位置不变。left的值表示对象左边框与浏览器窗口左边的距离right的值表示对象右边框与浏览器窗口右边的距离两者同时存在时，只有left起作用；如果两者都未指定，则其左边将与原文档流位置一致，即水平保持位置不变。 
在Position属性值为absolute的同时，如果有一级父对象（无论是父对象还是祖父对象，或者再高的辈分，一样）的Position属性值为Relative时，则上述的相对浏览器窗口定位将会变成相对父对象定位，这对精确定位是很有帮助的。

**relative**: 当Position属性值为Relative时对象原来占有的位置保留，其后面的对象按原来文档流仍然保持原来的位置Top的值表示对象相对原位置向下偏移的距离bottom的值表示对象相对原位置向上偏移的距离两者同时存在时，只有Top起作用。left的值表示对象相对原位置向右偏移的距离right的值表示对象相对原位置向左偏移的距离两者同时存在时，只有left起作用。

**fixed**: 生成固定定位的元素，相对于浏览器窗口进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。

## 实例
```HTML
<!DOCTYPE html>
<html>
    <head>
    <meta charset="utf-8"> 
    <title>Position测试</title> 
    <style>
        h2.pos_left
        {
        	position:relative;
        	left:-20px;
        }
        
        h2.pos_right
        {
        	position:relative;
        	left:20px;
        }
    </style>
    </head>
    
    <body>
        <h2>这是位于正常位置的标题</h2>
        <h2 class="pos_left">这个标题相对于其正常位置向左移动</h2>
        <h2 class="pos_right">这个标题相对于其正常位置向右移动</h2>
        <p>相对定位会按照元素的原始位置对该元素进行移动。</p>
        <p>样式 "left:-20px" 从元素的原始左侧位置减去 20 像素。</p>
        <p>样式 "left:20px" 向元素的原始左侧位置增加 20 像素。</p>
    </body>
</html>
```

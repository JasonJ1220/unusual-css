# pointer-events

## 说明
设置或检索在何时成为属性事件的target。

使用pointer-events来阻止元素成为鼠标事件目标不一定意味着元素上的事件侦听器永不会触发。如果元素后代明确指定了pointer-events属性并允许其成为鼠标事件的目标，那么指向该元素的任何事件在事件传播过程中都将通过父元素，并以适当的方式触发其上的事件侦听器。当然位于屏幕上在父元素上但不在后代元素上的鼠标活动都不会被父元素和后代元素捕获（将会穿过父元素而指向位于其下面的元素）。

## 语法
pointer-events：auto | none | visiblepainted | visiblefill | visiblestroke | visible | painted | fill | stroke | all

默认值：auto

## 取值
auto：
与pointer-events属性未指定时的表现效果相同。在svg内容上与visiblepainted值相同

none：
元素永远不会成为鼠标事件的target（就是鼠标事件完全失效）。但是，当其后代元素的pointer-events属性指定其他值时，鼠标事件可以指向后代元素，在这种情况下，鼠标事件将在捕获或冒泡阶触发父元素的事件侦听器。

---
其他值只能应用在SVG上。



## 实例
```HTML
<!DOCTYPE html>
<html lang="zh">

<head>
    <meta charset="utf-8" />
    <title>user-select</title>
    <meta name="author" content="JasonJ" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
    <style>
        a[href="http://www.baidu.com"] {
            pointer-events: none;
        }
    </style>
</head>

<body>
    <li><a href="http://www.sina.com">新浪（可以点击）</a></li>
	<li><a href="http://www.baidu.com">百度（无法点击）</a></li>
</body>

</html>
```

# user-select

## 说明
设置或检索是否允许用户选中文本。

## 语法

user-select: none | text | all | element

默认值: text

## 取值

none: 文本不能被选择

text: 可以选择文本

all: 在一个HTML编辑器中，当双击子元素或者上下文时，那么包含该子元素的最顶层元素也会被选中。

element: 允许选择在元素内开始; 但是，选择将包含在该元素的边界内。(仅IE支持)

auto: auto的计算值确定如下：

- 在 ::before 和 ::after 伪元素上，计算属性是 none
- 如果元素是可编辑元素，则计算值是 contain
- 否则，如果此元素的父元素的 user-select 的计算值为 all, 计算值则为 all
- 否则，如果此元素的父级上的 user-select 的计算值为 none, 计算值则为 none
- 否则，计算值则为 text

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
        .test {
            padding: 10px;
            -webkit-user-select: none;
            -moz-user-select: none;
            -o-user-select: none;
            user-select: none;
            background: #eee;
        }
    </style>
</head>

<body>
    <div class="test">你好，世界！</div>
    <div class="test">Bootstrap 是最受欢迎的 HTML、CSS 和 JS 框架，用于开发响应式布局、移动设备优先的 WEB 项目。</div>
</body>

</html>
```

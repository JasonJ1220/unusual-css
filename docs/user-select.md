# user-select

## 说明
设置或检索是否允许用户选中文本。

## 语法

user-select：none | text | all | element

默认值：text

## 取值

none：文本不能被选择

text：可以选择文本

all：当所有内容作为一个整体时可以被选择。如果双击或者在上下文上点击子元素，那么被选择的部分将是以该子元素向上回溯的最高祖先元素。

element：可以选择文本，但选择范围受元素边界的约束

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

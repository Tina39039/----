# 移动端开发注意事项
>
## 1.关于webkit内核中的一些私有的meta标签
>
* 强制让文档的宽度与设备的宽度保持1:1，并且文档的最大宽度比例为1.0，不允许用户点击屏幕放大浏览</br>
`<meta content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=0" name="viewport">`
>
* 允许全屏模式浏览------iPhone设备中safari私有meta标签</br>
`<meta content="yes" name="apple-mobile-web-app-capable">`
>
* safari顶端状态条的样式</br>
`<meta content="black" name="apple-mobile-web-app-status-bar-style">`
>
* 告诉设备忽略将页面中的数字识别为电话号码</br>
`<meta content="telephone=no" name="format-detection">`
>
## 2.如何去除Android平台中对邮箱地址的识别？
>
* 在iOS中是不会自动识别邮箱地址，但在Android平台则会自动检测邮箱地址，当用户触摸到邮箱地址时会弹出提示框提示用户发送邮件，如果不想让其自动识别页面中的邮箱地址，在head中加入`meta`标签</br>
`<meta content="email=no" name="format-detection"/>`
>
## 3.如何关闭iOS中键盘自动大写？
>
* 在iOS中，当虚拟键盘弹出时，默认情况下会开启首字母大写的功能。移动版webkit为input元素提供了autocapitalize属性。用`autocapitalize="off"`关闭键盘默认首字母大写
>
## 4.iOS禁止用户在新窗口打开页面,禁止用户保存/复制图片
>
* `-webkit-touch-callout:none`（仅适用于iOS）
>
## 5.iOS禁止用户选中文字
>
* `-webkit-user-select:none`
>


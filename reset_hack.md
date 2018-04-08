
# CSS
```css
/* 阻止旋转屏幕时自动调整字体大小 */
* {
  -webkit-text-size-adjust: none;
}

/* 修改移动端难看的点击的高亮效果，iOS和安卓下都有效 */
* {
  -webkit-tap-highlight-color: rgba(0,0,0,0);
}

/* 禁止 iOS 弹出各种操作窗口 */
.button {
  -webkit-touch-callout: none;
}

/* 禁止ios和android用户选中文字 */
.label {
  -webkit-user-select: none;
}

/* overflow-x: auto在iOS有兼容问题 */
table {
  -webkit-overflow-scrolling: touch;
}

/* 消除transition闪屏问题 */
.transition{
  /*1.设置内嵌的元素在 3D 空间如何呈现：保留 3D*/
  -webkit-transform-style: preserve-3d;
  /*2.(设置进行转换的元素的背面在面对用户时是否可见：隐藏)*/ 
  -webkit-backface-visibility: hidden; 
}

/* 防止上边距塌陷 */
div {
  &:before {
    content: '';
    display: table;
  }
}
```

# HTML
```html
<!-- 取消ios input首字母大写 -->
<input type="text" autocapitalize="none">

<!-- 禁止 iOS 识别长串数字为电话 -->
<meta name="format-detection" content="telephone=no" />


```

# 其他
- `position:absolute`插件解决iphone fixed元素中的input打开软键盘不定位的问题;
- 使用1. RAF增强, 2.css3替代, 3.硬件加速`transform: translate3d(0, 0, 0)` , 优化setTimeout/setInterval动画;
- iOS系统中文输入法输入英文时，字母之间可能会出现一个六分之一的空格 `this.value = this.value.replace(/\u2006/g, '');`

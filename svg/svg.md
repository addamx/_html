- 作为XML的一种方言，SVG必须正确的绑定命名空间 （在xmlns属性中绑定）。  
如何插入文档
- 如果HTML是XHTML并且声明类型为application/xhtml+xml，可以直接把SVG嵌入到XML源码中。
- 如果HTML是HTML5并且浏览器支持HTML5，同样可以直接嵌入SVG。然而为了符合HTML5标准，可能需要做一些语法调整。
- 可以通过 object 元素引用SVG文件：
`<object data="image.svg" type="image/svg+xml" />`
- 类似的也可以使用 iframe 元素引用SVG文件：
`<iframe src="image.svg"></iframe>`
- 理论上同样可以使用 img 元素
- 通过JavaScript动态创建并注入到HTML DOM中

HTTP head要求:
```http
Content-Type: image/svg+xml
Content-Encoding: gzip  //gzip压缩过
Vary: Accept-Encoding
```


API
- 基本形状
https://developer.mozilla.org/zh-CN/docs/Web/SVG/Tutorial/Basic_Shapes
- 路径
https://developer.mozilla.org/zh-CN/docs/Web/SVG/Tutorial/Paths
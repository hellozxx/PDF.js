# PDF.js
现在做的项目中有个需求：在线打开PDF文件。
试了iframe,但是存在跨域的问题，后台已经解决了跨域问题，并且文件地址在浏览器中是可以正常打开的，不明觉厉。
所以就使用了PDF.js

此项目的前端是用vue写的，需要安装PDF.js

<script src="//mozilla.github.io/pdf.js/build/pdf.js"></script>

命令： npm install pdf.js --save

所有的代码已上传，引用的时候，只需要传递pdfUrl即可。

刚使用的时候，有个坑，那就是渲染出来的PDF比较模糊，后来通过参考其他大牛的经验，发现需要更改一个参数

page.getViewport(2.0);

只要修改getViewport对应的参数，就可以解决模糊的问题。

另外，无论是pdf.js 还是Vue-pdf，都是不可以一次性加载完所有的PDF页面，而是一页一页的加载，所以我又做了翻页的效果。



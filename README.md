# FlexLayout
flexlayout website

##响应式布局，先看效果
###大屏效果：>50rem
![大图](https://raw.githubusercontent.com/wu0792/FlexLayout/master/doc/design/l.png)

###中屏效果：>30rem, <=50rem
![大图](https://raw.githubusercontent.com/wu0792/FlexLayout/master/doc/design/m.png)

###小屏效果：<30rem
![小图](https://raw.githubusercontent.com/wu0792/FlexLayout/master/doc/design/s.png)

###下面是一些笔记心得
================================================
PART I：
响应式网站的优点：
1 减少工作量
1）网站，设计，代码，内容都只有一份
2）JS,CSS做少量更改
2 节省时间
3 多个分辨率设备都能正确显示
4 搜索优化

缺点：
会加载更多的样式和脚本资源
设计比较难精确定位和控制
老版本浏览器的兼容问题

================================================
PART II：
主流浏览器
Chrome
IE/Edge（Edge : > 12)
Firefox
QQ（微信采用QQ浏览器X5的内核）
Safari/iOS Safari
360
UC
猎豹

================================================
PART III：
媒体查询 1
@media all and(min-width:800px) and (orientagion: landscape){
    ...
}

#逻辑操作查询符：not and only , (, 等同于 or)

#css3媒体属性
width: 视口宽度
height: 视口高度
device-width: 渲染表面的宽度，就是设备屏幕的宽度
device-height:渲染表面的高度，就是设备屏幕的高度

orientation:检查设备处于横向/纵向
aspect-ration:基于视口的宽高比
device-aspect-ratio: 渲染表面的宽度，就是设备屏幕的宽度
color:每种颜色的位数bits，比如 min-color:16位，8位
resolution:检测屏幕或打印机的分辨率，如： min-resolution:300dpi

以上属性都可以添加  min-  或 max-  前缀

================================================
媒体查询 2
width:  视口宽度
device-wdith

viewport 视口
针对PC，只有一个视口
针对移动设备，有三个视口：
布局视口(layout viewport)
可视视口(visual viewport)
理想视口(ideal viewport)

===============================================
**强制使用最新版本的IE文档模式**
```html
<meta http-equiv="x-ua-compatible" content="id=edge">
```

===============================================
**cssreset.css** 用来消除所有浏览器在一些默认样式上面的差异
**[normailize.css](https://necolas.github.io/normalize.css/)** 是 ** cssreset.css ** 的优化版本，使用更加广泛

===============================================
长度单位： px, em, rem
使用相对的值，不同的显示屏尺寸会有变化
px : 固定的单位
em : 相对的长度单位，参照了父元素的font-size，具有继承的特点，如果一直找父容器都找不到font-size，那会使用浏览器的默认em设置：1em = 16px
rem ：也是使用相对值，不过是参照了 html 元素，浏览器的默认值也是：1rem = 16px



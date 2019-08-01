点击体验→ <https://xuebihua.cn>

![xuebihua_qr](https://github.com/lmm214/xuebihua/blob/master/xuebihua_qr.png)

刷着阮一峰的 weekly 看到了 [Hanzi Writer](https://chanind.github.io/hanzi-writer/cn/) 这个项目，发现笔顺的动画比较自然，还能在 svg 上手写练习，最重要的是看看 demo 好像上手比较简单，实际也如此。功能代码非常好使，基本折腾在界面和陌生的代码上，比如想让 svg 自适应，搜索测试一晚发现还是以下代码好使：

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0">
```

考虑到教室大屏上不方便输入文字，直接内置一年级语文的400个生字，点击即可展示。发现，会 jQuery 还真省事！

考虑到大屏上输入文字不太方便，搜索一圈发现以下代码：[web版手写输入法](https://my.oschina.net/u/3112095/blog/3038734) ，利用了 QQ输入法的手写 [handwritingapi.js](http://s.pc.qq.com/webime/hw/js/handwritingapi.js) 接口，不过文中添加的仅是鼠标事件，移动端的触摸事件不支持，发现QQ输入法的鼠标定位值和 Canvas 直接触摸定位值不同，依样画葫芦造函数，神奇般的成了！

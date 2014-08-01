## 综述

Lazyload是基于KISSY MINI的懒加载组件

* 版本：2.0.0
* 作者：常胤
* demo：[http://kg.kissyui.com/lazyload/2.0.0/demo/index.html](http://kg.kissyui.com/lazyload/2.0.0/demo/index.html)

## 初始化组件
		
    S.use('kg/lazyload/2.0.0/index', function (S, Datalazyload) {
         var lazyload = new Datalazyload();
    })
	
	

## API说明



-  v0.01
-  [文档地址](http://changyin.demo.taobao.net/lazyload/)




### Configs

    threshold
    {Number} - 可选，设置后可以提前加载视窗以外的内容，提升体验

    event
    {String} - 可选，响应的事件，默认 "scroll touchmove resize"

    container
    {dom} - 可选，不设置则为document.body

    attribute
    {String} - 可选，设置需要lazyload的属性名，默认为data-ks-lazyload

    duration
    {Number} - 可选，延迟触发事件，默认 300ms

    load
    {Function} - 可选，每加载一个元素就会触发一次这个回调

    complete
    {Function} - 可选，所有元素加载完成后会触发此回调

    ### Methods

    refresh()
    强制立刻检测懒加载元素

    pause()
    暂停监控懒加载元素

    resume()
    继续监控懒加载元素

    destroy()
    停止监控并销毁组件


### 示例


```
KISSY.use("datalazyload",function(S,DataLazyLoad){

    new DataLazyLoad({
        load: function(el){
            console.log(el);
        },
        complete: function(){
            alert("加载完毕");
        }
    });

})
```


### DEMO

-  [普通demo](http://kg.kissyui.com/lazyload/2.0.0/demo/demo1.html)
-  [横向测试](http://kg.kissyui.com/lazyload/2.0.0/demo/demo1.html)
-  [淘宝detail](http://kg.kissyui.com/lazyload/2.0.0/demo/demo1.html)



### 移动设备测试

![DataLazyload](http://ma.taobao.com/qrcode/qrcode.do?activity=encode&text=http%253A%252F%252Fkg.kissyui.com%252Flazyload%252F2.0.0%252Fdemo%252Findex.html&channel_id=&width=300&height=300)







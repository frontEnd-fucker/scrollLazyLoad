# scrollLazyLoad

懒加载jQuery组件。
实现图片/区域懒加载。

```html
    <script src="jquery.min.js"></script> 
    <script src="jquery.scrollLazyLoad.js"></script> 
    <div class="header">...</div>
    <div class="main">
        <div class="holder">...</div>
        <div class="holder">...</div>
        <div class="holder">...</div>
        <div class="holder">...</div>
        <div class="container">
            <img src="" data-url="http://img.f2e.taobao.net/img.png?x=100x300" alt="" />
            <img src="" data-url="http://img.f2e.taobao.net/img.png?x=300x300" alt="" />
            <img src="" data-url="http://img.f2e.taobao.net/img.png?x=200x300" alt="" />
            <img src="" data-url="http://img.f2e.taobao.net/img.png?x=500x300" alt="" />
            <img src="" data-url="http://img.f2e.taobao.net/img.png?x=700x300" alt="" />
            <img src="" data-url="http://img.f2e.taobao.net/img.png?x=200x300" alt="" />
            <div data-url="temp.html"></div>   
        </div>
    </div>
```

```javascript
    /**
     * $('.container')为包含懒加载区域的选择器
     * @param {jQuery Element} 产生滚动条的区域，可省略，默认$(window)
     * @param {string} 懒加载路径的属性值，可省略，默认'data-url'
     * @param {function} 加载完毕后的回调函数，可省略
     */
    $('.container').scrollLazyLoad({
        scroller: $('.main'),
        attr: 'data-url',
        fn: function(){
            console.log('DONE!!!');
        }
    });
```

可下载demo，在服务器上运行window.html/scroller.html

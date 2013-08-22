# scrollLazyLoad

懒加载jQuery组件。

实现图片/区域懒加载。

使用该组件的方法：

## 1.引用jQuery库，引用scrollLazyLoad组件

```html
    <script src="jquery.min.js"></script> 
    <script src="jquery.scrollLazyLoad.js"></script> 
```

## 2.在需要进行懒加载的元素上设置data-url="..."，如果设置其他属性来存放路径，需要在初始化组件的时候配置参数

```html
    <img src="" data-url="..." alt="" />
    <div data-url="..."></div> 
```

## 3. 在包含懒加载元素的外层元素进行初始化，同时要说明产生滚动条的区域（window/局部区域）

```javascript
    /**
     * $('.container')为包含懒加载区域的外层元素
     * @param {jQuery Element} 产生滚动条的区域，可省略，默认window
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

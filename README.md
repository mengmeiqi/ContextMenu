# contextmenu
    右键菜单 使用javascript
## 知识点
### 原生js
#### 事件event:
        事件三要素：事件源、事件处理方法、事件对象
        浏览器是事件驱动的
#### 事件对象e:
        在function()里面其实带有一个参数e，e就是事件对象
        注：在IE8里面不支持e，所以用window.event
        e = e || window.event;
#### 阻止浏览器默认行为
        return false;
#### 在js中怎么获取事件源？
        不一定给谁绑定事件谁就是事件源。
        function getTarget(){
            e = e || window.event;
            return e.target(标准浏览器) || e.srcElement(早期IE);
        }
### javascript event对象的clientX,offsetX,screenX,pageX区别:
        event.clientX、event.clientY
        鼠标相对于浏览器窗口可视区域的X，Y坐标（窗口坐标），可视区域不包括工具栏和滚动条。IE事件和标准事件都定义了这2个属性
        event.pageX、event.pageY
        类似于event.clientX、event.clientY，但它们使用的是文档坐标而非窗口坐标。这2个属性不是标准属性，但得到了广泛支持。IE事件中没有这2个属性。
        event.offsetX、event.offsetY
        鼠标相对于事件源元素（srcElement）的X,Y坐标，只有IE事件有这2个属性，标准事件没有对应的属性。
        event.screenX、event.screenY
        鼠标相对于用户显示器屏幕左上角的X,Y坐标。标准事件和IE事件都定义了这2个属性
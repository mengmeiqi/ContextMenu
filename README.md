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


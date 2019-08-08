# dragtext
利用HTML的drag api编写的拖拽上方文本框中的文字到下方会生成新标签的程序
![img](https://github.com/mengliuchen/dragtext/blob/master/l5tzq-usy9a.gif)
案例地址：https://codepen.io/bigbybear469/pen/wVmWWO
#生成拖拽标签 
##开始拖拽

有一个用来存储拖拽事件参数的属性dataTransfer，进行拖放操作的时候，DataTransfer 对象用来保存，通过拖放动作，拖动到浏览器的数据。它可以保存一项或多项数据、一种或者多种数据类型。拖放的文字存储在dataTransfer中。

dataTransfer有两个方法setData()和getData()，用来存放数据和获取数据。dataTransfer.items和dataTransfer.files是数据和文件列表，使用getAsString方法可以拿到数据。

本例中的文本可以使用getData("text")直接获取。

```
        document.addEventListener("dragstart",function(e){
          var NY=false;
          var elemClassName=event.target.parentNode.className;
          e.dataTransfer.setData("NY",elemClassName == "tab"?true:false);
          console.log(e.dataTransfer.items)
        })
```
未完

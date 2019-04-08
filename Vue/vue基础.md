## 用法
1. Vue实例所控制的元素区（MVVM中的V）
> new的Vue实例，会控制这个元素中的所有内容
```
    <div id="app">
        <p>{{msg}}</p>
    </div>
```
2. 引入Vue的库
```
    <script src="lib/vue.js"></script>
```
3. 创建一个Vue实例（new出来的vm就是MVVM中的调度者）
> 当我们导入库之后，在浏览器的内存中，就多了一个Vue构造函数。
```
    var vm = new Vue({
        el:'#app',    //表示当前我们new的这个Vue实例，要控制页面上的哪个区域。
        （date就是MVVM中的m，专门用来保存每个页面中的数据）
        date:{   //date属性中，存放的是el中要用到的数据。
            msg:'欢迎学习Vue'
        }
    })
```

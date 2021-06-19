# HML语法参考<a name="ZH-CN_TOPIC_0000001115974722"></a>

-   [页面结构](#zh-cn_topic_0000001059340504_section1062764791514)
-   [数据绑定](#zh-cn_topic_0000001059340504_s8821c158917c48098219013e69129d1b)
-   [事件绑定](#zh-cn_topic_0000001059340504_s30850b61328e4359910467ab33b3e07d)
-   [列表渲染](#zh-cn_topic_0000001059340504_sb777d6d807fa43fea9be400b2600425b)
-   [条件渲染](#zh-cn_topic_0000001059340504_sf7f6eab2105a4030a1f34149417d6fc5)
-   [逻辑控制块](#zh-cn_topic_0000001059340504_s185169def14340fcbb12c3375cb0f0bb)
-   [模板引用](#zh-cn_topic_0000001059340504_section1388145672114)

HML（OpenHarmony Markup Language）是一套类HTML的标记语言，通过组件，事件构建出页面的内容。页面具备数据绑定、事件绑定、列表渲染、条件渲染和逻辑控制等高级能力。

## 页面结构<a name="zh-cn_topic_0000001059340504_section1062764791514"></a>

```
<!-- xxx.hml -->
<div class="item-container">
  <text class="item-title">Image Show</text>
  <div class="item-content">
    <image src="/common/xxx.png" class="image"></image>
  </div>
</div>
```

## 数据绑定<a name="zh-cn_topic_0000001059340504_s8821c158917c48098219013e69129d1b"></a>

```
<!-- xxx.hml -->
<div onclick="changeText">
  <text> {{content[1]}} </text>
</div>
```

```
// xxx.js
export default {
  data: {
    content: ['Hello World!', 'Welcome to my world!']
  },
  changeText: function() {
    this.content.splice(1, 1, this.content[0]);
  }
}
```

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   针对数组内的数据修改，请使用splice方法生效数据绑定变更。
>-   hml中的js表达式不支持ES6语法。

## 事件绑定<a name="zh-cn_topic_0000001059340504_s30850b61328e4359910467ab33b3e07d"></a>

事件绑定的回调函数接收一个事件对象参数，可以通过访问该事件对象获取事件信息。

```
<!-- xxx.hml -->
<div>
  <!-- 通过'@'绑定事件 -->
  <div @click="clickfunc"></div>
  <!-- 通过'on'绑定事件  -->
  <div onclick="clickfunc"></div>
  <!-- 使用事件冒泡模式绑定事件回调函数。5+ -->
  <div on:touchstart.bubble="touchstartfunc"></div>
  <!-- 使用事件捕获模式绑定事件回调函数。5+ -->
  <div on:touchstart.capture="touchstartfunc"></div>
  <!-- on:{event}等价于on:{event}.bubble。5+ -->
  <div on:touchstart="touchstartfunc"></div>
  <!-- 绑定事件回调函数，但阻止事件向上传递。5+ -->
  <div grab:touchstart.bubble="touchstartfunc"></div>
  <!-- 绑定事件回调函数，但阻止事件向下传递。5+ -->
  <div grab:touchstart.capture="touchstartfunc"></div>
  <!-- grab:{event}等价于grab:{event}.bubble。5+ -->
  <div grab:touchstart="touchstartfunc"></div>
</div>
```

```
// xxx.js
export default {
  data: {
    obj: '',
  },
  clickfunc: function(e) {
    this.obj = 'Hello World';
    console.log(e);
  },
}
```

-   示例

    ```
    <!-- xxx.hml -->
    <div class="container">
      <text class="title">{{count}}</text>
      <div class="box">
        <input type="button" class="btn" value="increase" onclick="increase" />
        <input type="button" class="btn" value="decrease" @click="decrease" />
        <!-- 传递额外参数 -->
        <input type="button" class="btn" value="double" @click="multiply(2)" />
        <input type="button" class="btn" value="decuple" @click="multiply(10)" />
        <input type="button" class="btn" value="square" @click="multiply(count)" />
      </div>
    </div>
    ```

    ```
    /* xxx.js */
    export default {
      data: {
        count: 0
      },
      increase() {
        this.count++;
      },
      decrease() {
        this.count--;
      },
      multiply(multiplier) {
        this.count = multiplier * this.count;
      }
    };
    ```

    ```
    /* xxx.css */
    .container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        left: 0px;
        top: 0px;
        width: 454px;
        height: 454px;
    }
    .title {
        font-size: 30px;
        text-align: center;
        width: 200px;
        height: 100px;
    }
    .box {
        width: 454px;
        height: 200px;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }
    .btn {
        width: 200px;
        border-radius: 0;
        margin-top: 10px;
        margin-left: 10px;
    }
    ```


## 列表渲染<a name="zh-cn_topic_0000001059340504_sb777d6d807fa43fea9be400b2600425b"></a>

```
<!-- xxx.hml -->
<div class="array-container">
  <!-- div列表渲染 -->
  <!-- 默认$item代表数组中的元素, $idx代表数组中的元素索引 -->
  <div for="{{array}}" tid="id" onclick="changeText">
    <text>{{$idx}}.{{$item.name}}</text>
  </div>
  <!-- 自定义元素变量名称 -->
  <div for="{{value in array}}" tid="id" onclick="changeText">    
    <text>{{$idx}}.{{value.name}}</text>
  </div>
  <!-- 自定义元素变量、索引名称 -->
  <div for="{{(index, value) in array}}" tid="id" onclick="changeText">    
    <text>{{index}}.{{value.name}}</text>
  </div>
</div>
```

```
// xxx.js
export default {
  data: {
    array: [
      {id: 1, name: 'jack', age: 18}, 
      {id: 2, name: 'tony', age: 18},
    ],
  },
  changeText: function() {
    if (this.array[1].name === "tony"){
      this.array.splice(1, 1, {id:2, name: 'Isabella', age: 18});
    } else {
      this.array.splice(2, 1, {id:3, name: 'Bary', age: 18});
    }
  },
}
```

tid属性主要用来加速for循环的重渲染，旨在列表中的数据有变更时，提高重新渲染的效率。tid属性是用来指定数组中每个元素的唯一标识，如果未指定，数组中每个元素的索引为该元素的唯一id。例如上述tid="id"表示数组中的每个元素的id属性为该元素的唯一标识。for循环支持的写法如下：

-   for="array"：其中array为数组对象，array的元素变量默认为$item。
-   for="v in array"：其中v为自定义的元素变量，元素索引默认为$idx。
-   for="\(i, v\) in array"：其中元素索引为i，元素变量为v，遍历数组对象array。

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   数组中的每个元素必须存在tid指定的数据属性，否则运行时可能会导致异常。
>-   数组中被tid指定的属性要保证唯一性，如果不是则会造成性能损耗。比如，示例中只有id和name可以作为tid字段，因为它们属于唯一字段。
>-   tid不支持表达式。

## 条件渲染<a name="zh-cn_topic_0000001059340504_sf7f6eab2105a4030a1f34149417d6fc5"></a>

条件渲染分为2种：if/elif/else和show。两种写法的区别在于：第一种写法里if为false时，组件不会在vdom中构建，也不会渲染，而第二种写法里show为false时虽然也不渲染，但会在vdom中构建；另外，当使用if/elif/else写法时，节点必须是兄弟节点，否则编译无法通过。实例如下：

```
<!-- xxx.hml -->
<div class="container">
  <button class="btn" type="capsule" value="toggleShow" onclick="toggleShow"></button>
  <button class="btn" type="capsule" value="toggleDisplay" onclick="toggleDisplay"></button>
  <text if="{{show}}"> Hello-One </text>
  <text elif="{{display}}"> Hello-Two </text>
  <text else> Hello-World </text>
</div>
```

```
// xxx.css
.container{
  flex-direction: column;
  align-items: center;
}
.btn{
  width: 280px;
  font-size: 26px;
  margin: 10px 0;
}
```

```
// xxx.js
export default {
  data: {
    show: false,
    display: true,
  },
  toggleShow: function() {
    this.show = !this.show;
  },
  toggleDisplay: function() {
    this.display = !this.display;
  }
}
```

优化渲染优化：show方法。当show为真时，节点正常渲染；当为假时，仅仅设置display样式为none。

```
<!-- xxx.hml -->
<div class="container">
  <button class="btn" type="capsule" value="toggle" onclick="toggle"></button>
  <text show="{{visible}}" > Hello World </text>
</div>
```

```
// xxx.css
.container{
  flex-direction: column;
  align-items: center;
}
.btn{
  width: 280px;
  font-size: 26px;
  margin: 10px 0;
}
```

```
// xxx.js
export default {
  data: {
    visible: false,
  },
  toggle: function() {
    this.visible = !this.visible;
  },
}
```

>![](public_sys-resources/icon-note.gif) **说明：** 
>禁止在同一个元素上同时设置for和if属性。

## 逻辑控制块<a name="zh-cn_topic_0000001059340504_s185169def14340fcbb12c3375cb0f0bb"></a>

<block\>控制块使得循环渲染和条件渲染变得更加灵活；block在构建时不会被当作真实的节点编译。注意block标签只支持for和if属性。

```
<!-- xxx.hml -->
<list>
  <block for="glasses">
    <list-item type="glasses">
      <text>{{$item.name}}</text>
    </list-item>
    <block for="$item.kinds">
      <list-item type="kind">
        <text>{{$item.color}}</text>
      </list-item>
    </block>
  </block>
</list>
```

```
// xxx.js
export default {
  data: {
    glasses: [
      {name:'sunglasses', kinds:[{name:'XXX',color:'XXX'},{name:'XXX',color:'XXX'}]},
      {name:'nearsightedness mirror', kinds:[{name:'XXX',color:'XXX'}]},
    ],
  },
}
```

## 模板引用<a name="zh-cn_topic_0000001059340504_section1388145672114"></a>

HML可以通过element引用模板文件，详细介绍可参考[自定义组件](基本用法.md#ZH-CN_TOPIC_0000001162494627)章节。

```
<!-- template.hml -->
<div class="item"> 
  <text>Name: {{name}}</text>
  <text>Age: {{age}}</text>
</div>
```

```
<!-- index.hml -->
<element name='comp' src='../../common/template.hml'></element>
<div>
  <comp name="Tony" age="18"></comp>
</div>
```


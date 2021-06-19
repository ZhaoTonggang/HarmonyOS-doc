# Props<a name="EN-US_TOPIC_0000001162414643"></a>

-   [Default Value](#en-us_topic_0000001059148556_section448655843113)
-   [Unidirectional Value Transfer](#en-us_topic_0000001059148556_section9681151218247)
-   [Monitoring Data Changes by $watch](#en-us_topic_0000001059148556_section205821113182114)
-   [Computed Property](#en-us_topic_0000001059148556_section1088954011234)

You can use  **props**  to declare attributes of a custom component. The attributes can be used by a parent component to pass parameters to a child component. Note that a camel case attribute name \(**compProp**\) should be converted to the kebab case format \(**comp-prop**\) when you reference the attribute in an external parent component. You can add  **props**  to a custom component, and pass the attribute to the child component.

```
<!-- comp.hml -->
<div class="item"> 
   <text class="title-style">{{compProp}}</text> 
</div>
```

```
// comp.js 
export default { 
  props: ['compProp'],
}
```

```
<!-- xxx.hml -->
<element name='comp' src='../../common/component/comp/comp.hml'></element>
<div class="container"> 
   <comp comp-prop="{{title}}"></comp> 
</div>
```

## Default Value<a name="en-us_topic_0000001059148556_section448655843113"></a>

You can set the default value for a child component attribute via  **default**. The default value is used if the parent component does not have  **default**  set. In this case, the  **props**  attribute must be in object format instead of an array.

```
<!-- comp.hml -->
<div class="item"> 
   <text class="title-style">{{title}}</text> 
</div>
```

```
// comp.js
export default { 
  props: {
    title: {
      default: 'title',
    },
  },
}
```

In this example, a  **<text\>**  component is added to display the title. The title content is a custom attribute, which displays the text specified by a user. If the user has not set a title, the default text will be displayed. Add the attribute when referencing the custom component.

```
<!-- xxx.hml -->
<element name='comp' src='../../common/component/comp/comp.hml'></element>
<div class="container"> 
<comp title=" Custom component "></comp>
</div>
```

## Unidirectional Value Transfer<a name="en-us_topic_0000001059148556_section9681151218247"></a>

Data can be transferred only from the parent component to child components. You are not allowed to change the value passed to the child component. However, you can receive the value passed by  **props**  as a default value in  **data**, and then change the  **data**  value.

```
// comp.js
export default { 
  props: ['defaultCount'],
  data() {
    return {
      count: this.defaultCount,
    };
  },
  onClick() {
    this.count = this.count + 1;
  },
}
```

## Monitoring Data Changes by  **$watch**<a name="en-us_topic_0000001059148556_section205821113182114"></a>

To listen for attribute changes in a component, you can use the  **$watch**  method to add a callback. The following code snippet shows how to use  **$watch**:

```
// comp.js
export default { 
  props: ['title'],
  onInit() {
    this.$watch('title', 'onPropertyChange');
  },
  onPropertyChange(newV, oldV) {
     console.info('title attribute changed'+ newV + ' ' + oldV)
  },
}
```

## Computed Property<a name="en-us_topic_0000001059148556_section1088954011234"></a>

To improve the development efficiency, you can use a computed property to pre-process an attribute in a custom component before reading or setting the attribute. In the  **computed**  field, you can set a getter or setter to be triggered when the attribute is read or written, respectively. The following is an example:

```
// comp.js
export default { 
  props: ['title'],
  data() {
    return {
      objTitle: this.title,
      time: 'Today',
    };
  },
  computed: {
    message() {
      return this.time + ' ' + this.objTitle;
    },
    notice: {
      get() {
        return this.time;
      },
      set(newValue) {
        this.time = newValue;
      },
    },
  },
  onClick() {
    console.info('get click event ' + this.message);
    this.notice = 'Tomorrow';
  },
}
```

The first computed property  **message**  has only a getter. The value of  **message**  changes depending on the  **objTitle**  value. The getter can only read but cannot set the value. You need a setter \(such as  **notice**  in the sample code\) to set the value of the computed property.


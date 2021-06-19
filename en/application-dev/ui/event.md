# Event<a name="EN-US_TOPIC_0000001063300566"></a>

-   [Gesture Events](#section21104561094)

Events mainly include gesture events for touchscreen devices.

## Gesture Events<a name="section21104561094"></a>

A gesture represents a semantic action \(for example, tap, drag, or longpress\) that can trigger one or more events. A gesture lifecycle may consist of multiple events from the start to the end of the gesture. The JS UI framework supports the following gesture events:

**Touch**

-   **touchstart**: Triggered when the touch starts
-   **touchmove**: Triggered when the touch moves
-   **touchcancel**: Triggered when the touch is interrupted, for example, by an incoming call notification or pop-up message
-   **touchend**: Triggered when the touch ends

**Click**

**click**: Triggered when a user taps the screen quickly.

**Longpress**

**longpress**: Triggered when a user keeps tapping the screen at the same position for a while.

The following is an example:

```
<!-- xxx.hml -->
<div class="container">
  <div class="text-container" onclick="click">
    <text class="text-style">{{onClick}}</text>
  </div>
  <div class="text-container" ontouchstart="touchStart">
    <text class="text-style">{{touchstart}}</text>
  </div>
  <div class="text-container" ontouchmove="touchMove">
    <text class="text-style">{{touchmove}}</text>
  </div>
  <div class="text-container" ontouchend="touchEnd">
    <text class="text-style">{{touchend}}</text>
  </div>
  <div class="text-container" ontouchcancel="touchCancel">
    <text class="text-style">{{touchcancel}}</text>
  </div>
  <div class="text-container" onlongpress="longPress">
    <text class="text-style">{{onLongPress}}</text>
  </div>
</div>
```

```
/* xxx.css */
.container {
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.text-container {
  margin-top: 10px;
  flex-direction: column;
  width: 750px;
  height: 50px;
  background-color: #09ba07;
}
.text-style {
  width: 100%;
  line-height: 50px;
  text-align: center;
  font-size: 24px;
  color: #ffffff;
}
```

```
// xxx.js
export default {
  data: {
    touchstart: 'touchstart',
    touchmove: 'touchmove',
    touchend: 'touchend',
    touchcancel: 'touchcancel',
    onClick: 'onclick',
    onLongPress: 'onlongpress',
  },
  touchCancel: function (event) {
    this.touchcancel = 'canceled';
  },
  touchEnd: function(event) {
    this.touchend = 'ended';
  },
  touchMove: function(event) {
    this.touchmove = 'moved';
  }, 
  touchStart: function(event) {
    this.touchstart = 'touched';
  },
  longPress: function() {
    this.onLongPress = 'longpressed';
  },
  click: function() {
    this.onClick = 'clicked';
  },
}
```


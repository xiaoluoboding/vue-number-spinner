# vue-number-spinner

[![npm](https://img.shields.io/npm/v/vue-number-spinner.svg?maxAge=2592000&style=flat-square)](https://www.npmjs.com/package/vue-number-spinner)
![Download](https://img.shields.io/npm/dt/vue-number-spinner.svg?style=flat-square)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/xiaoluoboding/vue-number-spinner/master/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/xiaoluoboding/vue-number-spinner.svg?style=flat-square)](https://github.com/xiaoluoboding/vue-number-spinner/stargazers)

Number spinner component for Vue.js. The number stepper widget, It allows users to type a value directly, or modify an existing value by spinning with the keyboard, mousewheel.

[![NPM](https://nodei.co/npm/vue-number-spinner.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/vue-number-spinner/)

# Installation

```bash
npm i vue-number-spinner -S
```

# Import

**ES6**
```javascript
import vueNumberSpinner from 'vue-number-spinner'
```

**CommonJS**

```javascript
var vueNumberSpinner = require('vue-number-spinner');
```

**script**

```javascript
<script type="text/javascript" src="vue/dist/vue.min.js"></script>
<script type="text/javascript" src="vue-number-spinner/dist/vue-number-spinner.min.js"></script>
<script type="text/javascript">
    var vueNumberSpinner = window['vue-number-spinner'];
</script>
```

# Basic Usage

**script**

```javascript
new Vue({
  el: 'body',
  components: { vueNumberSpinner }
});
```

**html**

```html
<!-- step by 1 -->
<vue-number-spinner :min=0 :max=10 :step=1></vue-number-spinner>
<!-- step by 5 -->
<vue-number-spinner :min=0 :max=100 :step=5></vue-number-spinner>
```

# Props

| Name  | Type | Desc  | Example  |
| :-------- | :--------:|:--------:|:--------:|
| min | Number  | The min value | 0 |
| max | Number  | The max value | 100 |
| step  | Number  | Increment/Decrement the value by step number | 5 |

# keyboard/mousewheel interaction

* `Up` Increment the value by one step.
* `Down` Decrement the value by one step.

# License

MIT

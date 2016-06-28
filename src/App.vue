<script>
import vueNumberSpinner from './vue-number-spinner.vue'

export default {
  data () {
    return {
      title: 'vue-number-spinner',
      stepByOne: '<vue-number-spinner :min=0 :max=10 :step=1></vue-number-spinner>'
    }
  },

  components: {
    'vue-number-spinner': vueNumberSpinner
  }
}
</script>

<template>
  <div id="app">
    <div id="wrapper">
      <h1><span v-text="title"></span></h1>
      <a href="#!" class="button">Source on GitHub</a>
      <div class="demo-container">
        <section class="demo-desc">
          <!-- <p>基于Vue.js的number spinner组件，支持按钮点击、键盘<kbd>↑</kbd><kbd>↓</kbd>、鼠标滚轮事件。</p> -->
          <p>Number spinner component for Vue.js, Easy to use.</p>
          <p>Support button click、keyboard <kbd>↑</kbd><kbd>↓</kbd> and mousewheel Event.</p>
        </section>
        <hr>
        <section class="demo-list">
          <div class="spinner-group number">
            <label class="label-control">Step By 1:</label>
            <vue-number-spinner :min=0 :max=10 :step=1></vue-number-spinner>
          </div>
          <div class="spinner-group number">
            <label class="label-control">Step By 5:</label>
            <vue-number-spinner :min=0 :max=100 :step=5></vue-number-spinner>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<style>
html {
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  overflow-x: hidden;
}

*,
*:before,
*:after {
  -webkit-box-sizing: inherit;
  -moz-box-sizing: inherit;
  box-sizing: inherit;
}

body {
  font-family: 'Source Sans Pro', 'Helvetica Neue', Arial, sans-serif;
  font-size: 15px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #34495e;
  margin: 0;
  border-top: 2px solid #4fc08d;
  background-color: #f8f8f8;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

h1 {
  font-family: 'Dosis', 'Source Sans Pro', 'Helvetica Neue', Arial, sans-serif;
  font-weight: 300;
  font-size: 4em;
  color: #2c3e50;
}

h4, a {
  font-weight: 400;
  font-size: 15px;
  color: #7f8c8d;
}

p {
  word-spacing: 0.05em;
}

a {
  text-decoration: none;
  color: #34495e;
}

a.button {
  display: inline-block;
  width: 280px;
  margin: 0.5em;
  font-family: 'Roboto Mono', Monaco, courier, monospace;
  font-weight: 700;
  color: #fff;
  background-color: #4fc08d;
  border-bottom: 2px solid #3aa373;
  padding: 12px 14px;
  border-radius: 4px;
  transition: all 0.15s ease;
}

a.button:hover {
  background-color: #5dc596;
  -webkit-transform: translate(0, -2px);
          transform: translate(0, -2px);
}

#social {
  text-align: center;
  list-style-type: none;
  margin: 0 auto;
  padding: 0;
  margin: 1.5em auto;
}

#wrapper {
  width: 650px;
  margin: 0 auto;
  min-height: 80px;
  text-align: center;
}

.demo-container {
  border: 2px solid #fff;
  border-radius: 2px;
  background-color: #FBFBFB;
  width: 100%;
  margin-top: 64px;
  padding: 10px;
}

.block{
  margin-top: 25px;
}

.reset-btn{
  outline: 0;
  cursor: pointer;
  padding: 7px 15px;
  border-radius: 2px;
  background-color: #58DCA1;
  color: #fff;
  font-weight: bold;
}

.label-control {
  position: relative;
  min-height: 1px;
  padding-left: 12px;
  width: 20%;
  text-align: right;
  float: left;
  margin: 4px 20px;
}

.spinner-group {
  margin-bottom: 15px;
}

.demo-desc {
  margin-bottom: 30px;
}

.demo-list {
  margin-top: 30px;
}

kbd {
  margin: 2px;
  padding: 2px 4px;
  font-size: 90%;
  color: #fff;
  background-color: #333;
  border-radius: 3px;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0,0,0,.25);
  box-shadow: inset 0 -1px 0 rgba(0,0,0,.25);
  vertical-align: middle;
}

hr {
  color: #eee;
  opacity: .1;
}

@media (max-width: 700px) {
  html,
  body {
      margin: 0;
  }
  #wrapper {
      width: 90%;
  }
}
</style>

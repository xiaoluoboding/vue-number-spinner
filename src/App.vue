<script>
import Spinner from './Spinner.vue'

export default {
  data () {
    return {
      msg: 'vue-number-spinner'
    }
  },

  components: {
    Spinner
  }
}
</script>

<template>
  <div id="app">
    <div id="wrapper">
      <h1>{{ msg }}</h1>
      <a href="#!" class="button">Source on GitHub</a>
      <div class="demo-container">
        <section class="desc">
          <p>说明：vue.js版本的number spinner组件，支持按钮、键盘、鼠标滑轮操作。</p>
        </section>
        <section class="demo">
          <div class="number">
            <label class="for-spinner">Number:</label>
            <spinner :min=-5 :max=25 :step=5></spinner>
          </div>
          <div class="currency">
            <label class="for-spinner">Currency:</label>
            <spinner :min=0 :max=10 :step=0.1></spinner>
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

.for-spinner {
  float: left;
  margin: 4px 20px;
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

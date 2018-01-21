<template>
  <div id="app">
    <img src="./assets/cat_sleep_dribbble.gif" width="300px" v-bind:class="{visible}">
    <HelloWorld v-bind:class="{visible}"/>
  <button v-bind:class="{visible}" @click="hidden=!hidden, visible=!visible">Let's wind down</button>
<div class="audiolist">
    <div class="player"><Audio1 v-bind:class="{hidden}"/></div>
  <div class="player"><Audio2 v-bind:class="{hidden}"/></div>
  <div class="player"><Audio3 v-bind:class="{hidden}"/></div>
  <div class="player"><Audio4 v-bind:class="{hidden}"/></div>
  </div>
  <div class="backbtn">
  <button v-bind:class="{hidden, back}" @click="hidden=!hidden, visible=!visible, back">Back</button>
  </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Audio1 from './components/Audio1'
import Audio2 from './components/Audio2'
import Audio3 from './components/Audio3'
import Audio4 from './components/Audio4'


export default {
  name: 'App',
  data () {
    return {
      hidden: true,
      visible:false,
      back: true

    }
  },
  components: {
    HelloWorld,
    Audio1,
    Audio2,
    Audio3,
    Audio4
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #7B8DAD;
  margin-top: 60px;
}
body {
background-color: #182435;
}
.audiolist {
  display: grid;
  grid-template-columns: repeat(2, 180px);
  grid-gap: 5px;
}

.hidden {
  display: none;
}
.visible {
  display: none;
}
.backbtn {
  position: fixed;
 margin: 0 auto;
 left: 2em;
 bottom: 2em;
}
button {
  color: #C6CDE0;
  font-size: 1em;
  border: solid 1px #7B8DAD;
  border-radius: 3px;
  background-color: transparent;
  padding: 10px;
  margin-bottom: 2em;
}

</style>

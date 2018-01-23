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
  <div class="player"><GlobalControls v-bind:class="{hidden}"/></div>
  </div>
  <div class="backbtn">
  <button v-bind:class="{hidden, back}" @click="hidden=!hidden, visible=!visible, back"><</button>
  </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Audio1 from './components/Audio1'
import Audio2 from './components/Audio2'
import Audio3 from './components/Audio3'
import Audio4 from './components/Audio4'
import GlobalControls from './components/GlobalControls'


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
    Audio4,
    GlobalControls
  }
}
</script>

<style>

  :root {
  --light-grey: #7B8DAD;
  --bcolor: #182435;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--light-grey);
  margin-top: 70px;

}
body {
  background-color: var(--bcolor);
}
.audiolist {
  height: 100%;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 5px;
  padding:5px;
  margin: 0 auto;
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
 top: 2em;
}
.backbtn :hover {
  background-color: var(--light-grey);
  color: var(--bcolor);
}

button {
  color: #C6CDE0;
  font-size: 1em;
  border: solid 1px var(--light-grey);
  border-radius: 3px;
  background-color: var(--bcolor);
  padding: 10px 20px;
  margin-bottom: 2em;
}



</style>

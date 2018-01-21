<template lang="html">
  <div id="audio1">
  <p>Rain</p>
  <audio id="audio1_2" ref="audio" src="" loop></audio>
  <div class="controls1">
  <button ref="playBtn" v-on:click="play">Play </button>
  <button v-bind:class="{hidden}" @click="hidden=!hidden, visible=!visible" v-on:click="play">Pause</button>
  </br>
  <input id="volume" class="gain" type="range" v-model="volumeVal" min="0" max="1" step="0.001" value="0.2"></input>
  <div> {{ volumeVal }}</div>
  </div>
  </div>
</template>

<script>
export default {
  name: "Audio1",
  data() {
    return {
      audioOne: new Audio("https://www.dropbox.com/s/iozko5ymc63rv0b/rain.mp3?dl=1"),
      volumeVal: "0.2",
      hidden: true,
      visible:false


    }
  },
  methods: {
    play: function(event) {
      var a = this.audioOne;
      a.oncanplaythrough = isAppLoaded;
      a.loop = true;
      var playBtn = this.$refs.playBtn;
      a.volume = this.volumeVal;
      if (a.paused) {
        a.play();
        playBtn.textContent= "Pause";
      } else {
        a.pause();
        playBtn.textContent= "Play";
      }
    }
  },
  watch: {
    volumeVal: function(val, oldVal){
      this.audioOne.volume = val;
      }

  }
}

</script>

<style scoped>

button {
  width: 120px;
  height: 120px;
  background-image: url("../assets/rain.gif");
  border: none;
}
input[type=range] {
  -webkit-appearance: none;
  margin: 5px 0;
  width: 68%;
}
input[type=range]:focus {
  outline: none;
}
input[type=range]::-webkit-slider-runnable-track {
  width: 68%;;
  height: 2px;
  cursor: pointer;
  animate: 0.2s;
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
  background: #7b8dad;
  border-radius: 2px;
  border: 0px solid #000101;
}
input[type=range]::-webkit-slider-thumb {
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
  border: 0px solid #000000;
  height: 20px;
  width: 20px;
  border-radius: 20px;
  background: #7b8dad;
  cursor: pointer;
  -webkit-appearance: none;
margin-top: -9px;
}
input[type=range]:focus::-webkit-slider-runnable-track {
  background: #c6cde0;
}
input[type=range]:focus::-webkit-slider-thumb {
  background: #c6cde0;
  border: 2px solid #7b8dad;
}
input[type=range]::-moz-range-track {
  width: 100%;
  height: 12.8px;
  cursor: pointer;
  animate: 0.2s;
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
  background: #7b8dad;
  border-radius: 25px;
  border: 0px solid #000101;
}
input[type=range]::-moz-range-thumb {
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
  border: 0px solid #7b8dad;
  height: 20px;
  width: 39px;
  border-radius: 7px;
  background: #7b8dad;
  cursor: pointer;
}
input[type=range]::-ms-track {
  width: 100%;
  height: 12.8px;
  cursor: pointer;
  animate: 0.2s;
  background: #7b8dad;
  border-color: transparent;
  border-width: 39px 0;
  color: transparent;
}
input[type=range]::-ms-fill-lower {
  background: #7b8dad;
  border: 0px solid #000101;
  border-radius: 50px;
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
}
input[type=range]::-ms-fill-upper {
  background: white;
  border: 0px solid #000101;
  border-radius: 50px;
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
}
input[type=range]::-ms-thumb {
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
  border: 0px solid #000000;
  height: 20px;
  width: 39px;
  border-radius: 7px;
  background: #7b8dad;
  cursor: pointer;
}
input[type=range]:focus::-ms-fill-lower {
  background: #c6cde0;
}
input[type=range]:focus::-ms-fill-upper {
  background: #c6cde0;
}

body {
  padding: 30px;
}
</style>

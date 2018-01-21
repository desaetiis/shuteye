<template lang="html">
  <div id="audio1">
  <p>Rain</p>

<audio id="audio1_2" ref="audio" src="http://file.kuyinyun.com/group2/M00/EF/C0/rBBGelUPiWiACpYhAAQfE72-jHE679.mp3" loop></audio>
<div class="controls1">
  <button ref="playBtn" v-on:click="play">Play </button>
  <button v-bind:class="{hidden}" @click="hidden=!hidden, visible=!visible" v-on:click="play">Pause</button>
  </br>
  <input id="volume" type="range" v-model="volumeVal" min="0" max="1" step="0.001" value="0.2"></input>
  <div> {{ volumeVal }}</div>

  </div>
  </div>
</template>

<script>
export default {
  name: "Audio1",
  data() {
    return {
      audioOne: new Audio("http://file.kuyinyun.com/group2/M00/EF/C0/rBBGelUPiWiACpYhAAQfE72-jHE679.mp3"),
      volumeVal: "0.2",
      hidden: true,
      visible:false


    }
  },
  methods: {
    play: function(event) {
      var a = this.audioOne;
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
  created() {
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
input #volume{
  width:10%;
  background:#111;
  height:1px;
  margin-bottom:20px;
}
input #volume::-webkit-slider-thumb{
  background:#fff;
  height:20px;
  width:100px;
  display: block;
}

</style>

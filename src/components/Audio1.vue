<template lang="html">
  <div id="audio1" v-bind:class="{hidden:hidden}">
  <p>Rain</p>
<audio volume="0.1" id="audio1_2" src="http://file.kuyinyun.com/group2/M00/EF/C0/rBBGelUPiWiACpYhAAQfE72-jHE679.mp3" loop></audio>
<div class="controls1">
  <button onclick="document.getElementById('audio1_2').play()">Play</button>
  <button onclick="document.getElementById('audio1_2').pause()">Pause</button>
  <button onclick="document.getElementById('audio1_2').volume -= 0.1">Vol- </button>
  <button onclick="document.getElementById('audio1_2').volume += 0.1">Vol+ </button>

  </div>
  </div>
</template>

<script>
export default {
  name: "Audio1",
  data () {
    return {

    }
  }
}
</script>

<style scoped>

</style>

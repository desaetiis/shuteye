<template lang="html">
<div id="audio4">
  <p>Waterfall</p>
  <audio volume="0.1" id="audio4_2"src="http://file.kuyinyun.com/group2/M00/61/1A/rBBGelcTAZCAcQ4cAAcmErMReH4964.mp3" loop></audio>
<div class="controls4">
  <button onclick="document.getElementById('audio4_2').play()">Play</button>
  <button onclick="document.getElementById('audio4_2').pause()">Pause</button>
  <button onclick="document.getElementById('audio4_2').volume -= 0.1">Vol- </button>
  <button onclick="document.getElementById('audio4_2').volume += 0.1">Vol+ </button>

  </div>
  </div>
</template>

<script>
export default {
  name: "Audio4",
  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>

</style>

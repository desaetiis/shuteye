<template lang="html">
<div id="audio2">
  <p>Birds</p>
  <audio volume="0.1" id="audio2_2" src="http://file.kuyinyun.com/group1/M00/94/83/rBBGdFYkXFuAYuTRAA2ax4_NmEk387.mp3" loop>

  </audio>
<div class="controls2">
<button onclick="document.getElementById('audio2_2').play()">Play</button>
  <button onclick="document.getElementById('audio2_2').pause()">Pause</button>
  <button onclick="document.getElementById('audio2_2').volume -= 0.1">Vol- </button>
  <button onclick="document.getElementById('audio2_2').volume += 0.1">Vol+ </button>

  </div>
  </div>
</template>

<script>
export default {
	name: "Audio2",
  data () {
    return {

    }
  },
  methods: {

  }
}
</script>

<style scoped>

</style>

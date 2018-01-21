<template lang="html">
<div id="audio3">
  <p>Ocean</p>
  <audio volume="0.1" id="audio3_2" src="http://file.kuyinyun.com/group2/M00/84/DF/rBBGelZL7EuAKFL_ABiwByGtPBo792.mp3"  loop>

  </audio>
<div class="controls3">
  <button onclick="document.getElementById('audio3_2').play()">Play</button>
  <button onclick="document.getElementById('audio3_2').pause()">Pause</button>
  <button onclick="document.getElementById('audio3_2').volume -= 0.1">Vol- </button>
  <button onclick="document.getElementById('audio3_2').volume += 0.1">Vol+ </button>

  </div>
  </div>
</template>

<script>
export default {
	name: "Audio3",
  data () {
    return {

    }
  }
}
</script>

<style>


</style>

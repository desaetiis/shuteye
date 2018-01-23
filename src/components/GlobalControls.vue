<template lang="html">
  <div id="global_controls">
  <span>Play</span>
<span>Stop</span>
  <span>Volume</span>


</div>
</template>

<script>
export default {
  name: "GlobalControls",
  data() {
    return {



    }
  },
  methods: {

  },
  watch: {

  }
}

</script>

<style scoped>
#global_controls {
  height: 60px;
  width: 100%;
  position: fixed;
  bottom: 0;
  left: 0;
  background-color: var(--light-grey);
}
span {
  color: var(--bcolor);
}
button {
  width: 120px;
  height: 120px;
  border: 1px solid var(--light-grey);
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
  background: var(--light-grey);
  border-radius: 2px;
  border: 0px solid #000101;
}
input[type=range]::-webkit-slider-thumb {
  box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
  border: 0px solid #000000;
  height: 20px;
  width: 20px;
  border-radius: 20px;
  background: var(--light-grey);
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
  background: var(--light-grey);
  cursor: pointer;
}
input[type=range]::-ms-track {
  width: 100%;
  height: 12.8px;
  cursor: pointer;
  animate: 0.2s;
  background: var(--light-grey);
  border-color: var(--b-color);
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

</style>

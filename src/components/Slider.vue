<template>
  <div class="container">
    <b :style="{ color: color}" class="sliderTitle">{{title}}</b> <b>{{value}}</b>
    <input id="slider" accept="image/png, image/jpg, image/jpeg" v-model="value" type="range" min="-100" max="100" value="0" :class="type" :disabled="isDisabled" @input="$emit('valueChanged', {type: type, value: $event.target.value})">
    <p class="sliderSubtitle">{{subtitle}}</p>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  props: {
    type: String,
    title: String,
    subtitle: String,
    color: String,
    isDisabled: Boolean
  },

  data: function() {
    return {
      value: 0
    }
  }
}
</script>

<style scoped lang="scss">
// base input style
input[type=range] {
  height: 0.35em;
  -webkit-appearance: none;
  width: 98%;

  //position: relative;
  //overflow: hidden;
}
input[type=range]:focus {
  outline: none;
}
input[type=range]::-webkit-slider-runnable-track {
  width: 100%;
  height: 0.35em;
  cursor: pointer;
  animate: 0.2s;
  box-shadow: 0px 0px 0px #000000;
  border-radius: 0.5em;
  border: 0px solid #000000;
}

input[type=range]::-webkit-slider-thumb {
  box-shadow: 0px 0px 0px #000000;
  //box-shadow: -100vw 0 0 100vw dodgerblue;
  border: 0.25em solid #FFFFFF;
  height: 1.4em;
  width: 1.4em;
  border-radius: 50%;
  cursor: pointer;
  -webkit-appearance: none;
  margin-top: -0.55em;
}

input[type=range]::-moz-range-track {
  width: 100%;
  height: 0.35em;
  cursor: pointer;
  animate: 0.2s;
  box-shadow: 0px 0px 0px #000000;
  border-radius: 0.5em;
  border: 0px solid #000000;
}

input[type=range]::-moz-range-progress {
  height: 0.35em;
  border-radius: 0.5em;
}

input[type=range]::-moz-range-thumb {
  box-shadow: 0px 0px 0px #000000;
  border: 0.25em solid #FFFFFF;
  height: 1.1em;
  width: 1.1em;
  border-radius: 50%;
  cursor: pointer;
}
input[type=range]::-ms-track {
  width: 100%;
  height: 0.35em;
  cursor: pointer;
  animate: 0.2s;
  background: transparent;
  border-color: transparent;
  color: transparent;
  border-radius: 0.5em;
}
input[type=range]::-ms-fill-lower {
  border: 0px solid #000000;
  border-radius: 0.5em;
  box-shadow: 0px 0px 0px #000000;
}
input[type=range]::-ms-fill-upper {
  border: 0px solid #000000;
  border-radius: 0.5em;
  box-shadow: 0px 0px 0px #000000;
}
input[type=range]::-ms-thumb {
  margin-top: 1px;
  box-shadow: 0px 0px 0px #000000;
  border: 0.25em solid #FFFFFF;
  height: 1.1em;
  width: 1.1em;
  border-radius: 50%;
  cursor: pointer;
}

// custom styles - brightness
.brightness::-webkit-slider-runnable-track {
  background: #25A95B;
}

.brightness:disabled::-webkit-slider-runnable-track {
  background: #C8E9D6;
}

.brightness::-webkit-slider-thumb {
  background: #25A95B;
}

.brightness:disabled::-webkit-slider-thumb {
  background: #C8E9D6;
}

.brightness:focus::-webkit-slider-runnable-track {
  background: #25A95B;
}

.brightness::-moz-range-track {
  background: #C8E9D6;
}

.brightness::-moz-range-progress {
  background-color: #25A95B;
}

.brightness:disabled::-moz-range-progress {
  background: #C8E9D6;
}

.brightness::-moz-range-thumb {
  background: #25A95B;
}

.brightness:disabled::-moz-range-thumb {
  background: #C8E9D6;
}

.brightness::-ms-fill-lower {
  background: #25A95B;
}

.brightness:disabled::-ms-fill-lower {
  background: #C8E9D6;
}

.brightness::-ms-fill-upper {
  background: #C8E9D6;
}

.brightness::-ms-thumb {
  background: #25A95B;
}

.brightness:disabled::-ms-thumb {
  background: #C8E9D6;
}

.brightness:focus::-ms-fill-lower {
  background: #25A95B;
}

.brightness:focus::-ms-fill-upper {
  background: #25A95B;
}

// custom styles - contrast
.contrast::-webkit-slider-runnable-track {
  background: #4A90E2;
}

.contrast:disabled::-webkit-slider-runnable-track {
  background: #C8DBE9;
}

.contrast::-webkit-slider-thumb {
  background: #4A90E2;
}

.contrast:disabled::-webkit-slider-thumb {
  background: #C8DBE9;
}

.contrast:focus::-webkit-slider-runnable-track {
  background: #4A90E2;
}

.contrast::-moz-range-track {
  background: #C8DBE9;
}

.contrast::-moz-range-progress {
  background-color: #4A90E2;
}

.contrast:disabled::-moz-range-progress {
  background-color: #C8DBE9;
}

.contrast::-moz-range-thumb {
  background: #4A90E2;
}

.contrast:disabled::-moz-range-thumb {
  background: #C8DBE9;
}

.contrast::-ms-fill-lower {
  background: #4A90E2;
}

.contrast:disabled::-ms-fill-lower {
  background: #C8DBE9;
}

.contrast::-ms-fill-upper {
  background: #C8DBE9;
}

.contrast::-ms-thumb {
  background: #4A90E2;
}

.contrast:disabled::-ms-thumb {
  background: #C8DBE9;
}

.contrast:focus::-ms-fill-lower {
  background: #4A90E2;
}

.contrast:focus::-ms-fill-upper {
  background: #4A90E2;
}

// container
.container {
  border-radius: 0.3em;
  padding: 0.8em 1em 0.15em 1em;

  box-shadow: 0px 0px 10px 0px rgba(214, 214, 214, 0.75);
  -moz-box-shadow: 0px 0px 10px 0px rgba(214, 214, 214, 0.75);
  -webkit-box-shadow: 0px 0px 10px 0px rgba(214, 214, 214, 0.75);
  -o-box-shadow: 0px 0px 10px 0px rgba(214, 214, 214, 0.75);
}

.sliderTitle {
  font-size: 1.1em;
  //font-family: 'Graphik-Medium';
}

.sliderSubtitle {
  font-size: 0.9em;
  color: #44526D;
  margin-top: 0.8em;
}
</style>

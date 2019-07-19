<template>
  <div class="container">
    <h1>Hello Test</h1>

    <button v-if="audioPlaying" @click="playQuizzAudio('audio')" class="btn">
      <i class="fa fa-play"></i>
    </button>

    <button v-else @click="pauseQuizzAudio('audio')" class="btn">
      <i class="fa fa-pause"></i>
    </button>

    <button @click="speedUpAudio('audio')" class="btn">
      <i class="fa fa-home"></i>
    </button>
    <input
      type="range"
      v-model="rate"
      min="0.5"
      max="2"
      step="0.1"
      class="slider"
      @change="changeSpeed('audio', rate)"
    />
    <audio :src="s" controls="false" preload="metadata" style="display:none" id="audio"></audio>
  </div>
</template>

<script>
export default {
  data() {
    return {
      rate: null,
      audioPlaying: true,
      s:
        'http://download1638.mediafire.com/ywhbf0jm1nug/2p8rc3l1yyq20x8/Bubba%5C%27s+Food+Audio.mp3'
    }
  },
  methods: {
    playQuizzAudio(id) {
      const self = this
      window.jQuery(document).ready(function() {
        const audio = window.jQuery(this).find(id)
        audio.trigger('play')
        self.audioPlaying = false
      })
    },
    pauseQuizzAudio(id) {
      const self = this
      self.audioPlaying = true
      window.jQuery(document).ready(function() {
        const audio = window.jQuery(this).find(id)
        audio.trigger('pause')
      })
    },
    changeSpeed(id, rate) {
      const self = this
      window.jQuery(document).ready(function() {
        const audio = window.jQuery(this).find(id)
        audio.playbackRate = rate
        console.log(audio.playbackRate)
      })
    }
  }
}
</script>

<style>
.slidecontainer {
  width: 100%;
}

.slider {
  -webkit-appearance: none;
  width: 100%;
  height: 25px;
  background: #d3d3d3;
  outline: none;
  opacity: 0.7;
  -webkit-transition: 0.2s;
  transition: opacity 0.2s;
}

.slider:hover {
  opacity: 1;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 25px;
  height: 25px;
  background: #4caf50;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 25px;
  height: 25px;
  background: #4caf50;
  cursor: pointer;
}
</style>

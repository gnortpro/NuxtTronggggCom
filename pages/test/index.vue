<template>
  <div class="container">
    <h1>Hello Test</h1>

    <button v-if="audioPlaying" @click="play('audio')" class="btn">
      <i class="fa fa-play"></i>
    </button>

    <button v-else @click="pause()" class="btn">
      <i class="fa fa-pause"></i>
    </button>
    <button class="btn" @click="stop()">Stop</button>
    <button class="btn" @click="changeLoop()">Loop {{this.innerLoop}}</button>
    <div>
      Progress:
      <div class="progressbar">
        <!-- <input type /> -->
        <div class="progresswidth" :style="progressStyle"></div>
      </div>Speed:
      <input
        id="audioSpeed"
        type="range"
        v-model="speed"
        min="0.5"
        max="2"
        step="0.1"
        class="slider"
        @change="changeSpeed()"
      />
      Volume:
      <input
        id="audioSpeed"
        type="range"
        v-model="volume"
        min="0"
        max="1"
        step="0.1"
        class="slider"
        @change="changeVolume()"
      />
    </div>
    <audio :src="s" preload="auto" style="display:none" id="audio"></audio>
  </div>
</template>

<script>
export const convertTimeHHMMSS = val => {
  let hhmmss = new Date(val * 1000).toISOString().substr(11, 8)
  return hhmmss.indexOf('00:') === 0 ? hhmmss.substr(3) : hhmmss
}
export default {
  data() {
    return {
      progressStyle: '',
      currentTime: '00:00',
      audio: undefined,
      volume: 0.5,
      speed: 1,
      loaded: false,
      innerLoop: undefined,
      audioPlaying: true,
      totalDuration: 0,
      s: 'https://sample-videos.com/audio/mp3/crowd-cheering.mp3'
    }
  },
  computed: {
    duration: function() {
      return this.audio ? convertTimeHHMMSS(this.totalDuration) : ''
    }
  },
  methods: {
    play(id) {
      const self = this
      window.jQuery(document).ready(function() {
        const audio = window.jQuery(this).find(id)
        audio.trigger('play')
        self.audioPlaying = false
      })
      // this.audio.play()
      // this.audioPlaying = false
    },
    pause() {
      // const self = this
      // self.audioPlaying = true
      // window.jQuery(document).ready(function() {
      //   const audio = window.jQuery(this).find(id)
      //   audio.trigger('pause')
      // })
      this.audio.pause()
      this.audioPlaying = true
    },
    stop() {
      this.audio.pause()
      this.audio.currentTime = 0
    },
    changeSpeed(id) {
      // const self = this
      // window.jQuery(document).ready(function() {
      //   const audio = window.jQuery(id)[0]
      //   audio.playbackRate = rate
      // })
      this.audio.playbackRate = this.speed
    },
    changeLoop() {
      this.innerLoop = !this.innerLoop
      this.audio.loop = this.innerLoop
    },
    changeVolume(id) {
      // const self = this
      // window.jQuery(document).ready(function() {
      //   const audio = window.jQuery(id)[0]
      //   audio.volume = volume
      // })
      this.audio.volume = this.volume
    },
    loadedFileOnStart() {
      if (this.audio.readyState >= 2) {
        if (this.autoPlay) this.play()

        this.loaded = true
        this.totalDuration = parseInt(this.audio.duration)
        console.log(this.totalDuration)
      } else {
        throw new Error('Failed to load sound file')
      }
    },
    playingProgressbarUI() {
      let currTime = parseInt(this.audio.currentTime)
      let percentage = parseInt((currTime / this.totalDuration) * 100)
      this.progressStyle = `width:${percentage}%;`
      this.currentTime = convertTimeHHMMSS(currTime)
      console.log(this.currentTime)
    },
    handlePlayPause: function(e) {
      if (e.type === 'pause' && this.playing === false) {
        this.progressStyle = `width:0%;`
        this.currentTime = '00:00'
        this.paused = true
      }
    },
    getAudio: function() {
      return this.$el.querySelectorAll('audio')[0]
    },
    init() {
      this.audio.addEventListener('loadeddata', this.loadedFileOnStart)
      this.audio.addEventListener('timeupdate', this.playingProgressbarUI)
      this.audio.addEventListener('pause', this.handlePlayPause)
      this.audio.addEventListener('play', this.handlePlayPause)
    }

    // changeS() {
    //   window.jQuery(document).ready(function() {
    //     const audio = window.jQuery('audio')
    //     audio.playbackRate = 2
    //     console.log(audio.playbackRate)
    //   })
    // }
  },
  mounted() {
    this.audio = this.getAudio()
    this.init()
  },
  watch: {}
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
.progressbar {
  height: 50px;
  background: aquamarine;
  position: relative;
  width: 700px;
}

.progresswidth {
  height: auto;
  background: black;
  position: absolute;
  top: 0;
  bottom: 0;
}
</style>

<template>
  <div id="app">
    <div
      style="
      position: absolute;
      bottom:10px;
      left: 0;
      width: 100%;
      height: 100px;
      z-index: 99;
      display: flex;
      justify-content: space-between"
    >
      <button class="btn-main btn-main__left" @click="goBack">{{ `&#8656;` }}</button>
      <button class="btn-main btn-main__rigth" @click="goForvard">{{ `&#8658;` }}</button>
    </div>
      <my-start v-if="currentSlide === 1"></my-start>
      <my-sky
         v-if="currentSlide === 2"
         :sheetParam='sheetParams[0]'
      ></my-sky>
      <my-sky v-if="currentSlide === 3" :sheetParam="sheetParams[1]"></my-sky>
      <my-ss v-if="currentSlide === 4"></my-ss>
      <my-sun v-if="currentSlide === 5"></my-sun>
      <my-ice v-if="currentSlide === 6"></my-ice>
      <my-end v-if="currentSlide === 7"></my-end>
  </div>
</template>

<script>
import Start from './Start'
import Sky from './Sky'
import SS from './SS'
import ice from './noSun'
import Sun from './Sun'
import End from './end'

export default {
  name: 'app',
  data () {
    return {
      currentSlide: 1,
      title: [
        'Звезды',
        'Солнце и люди'
      ],
      sheetParams: [
        {
          title: 'Звезды',
          class: 'sky-url',
          left: false
        },
        {
          title: 'Солнце и люди',
          class: 'people-url',
          left: true
        }
      ]
    }
  },
  components: {
    myStart: Start,
    mySky: Sky,
    mySs: SS,
    myIce: ice,
    mySun: Sun,
    myEnd: End
  },
  methods: {
    onKeyPress (event) {
      event.preventDefault()
      if (event.keyCode === 39) {
        this.goForvard()
      }
      if (event.keyCode === 37) {
        this.goBack()
      }
    },
    goForvard () {
      this.currentSlide++
      if (this.currentSlide > 7) {
        this.currentSlide = 1
      }
    },
    goBack () {
      this.currentSlide--
      if (this.currentSlide <= 1) {
        this.currentSlide = 7
      }
    }
  },
  mounted: function () {
    document.addEventListener('keydown', this.onKeyPress)
  }
}
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    width: 100%;
    height: 100%;
  }
  .slide-fade-enter-active {
    transition: all .3s ease;
  }
  .slide-fade-leave-active {
    transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
  }
  .slide-fade-enter, .slide-fade-leave-to
    /* .slide-fade-leave-active до версии 2.1.8 */ {
    opacity: 0;
  }

  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  .btn-main {
    width: 80px;
    height: 80px;
    background: rgba(255, 255, 255, .25);
    color: rgba(255, 255, 255, .45);
    font-size: 40px;
    border: none;

  }
  .btn-main__rigth {
    border-radius: 50% 0 0 50%;
  }
  .btn-main__left {
    border-radius: 0 50% 50% 0;
  }

  .btn-main:hover {
    background: rgba(255, 255, 255, .5);
    color: rgba(255, 0, 0 , 0.5);
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>

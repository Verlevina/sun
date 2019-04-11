<template>
  <div id="app">
    <div style="position: absolute; top:50%; left: 0; width: 100%; height: 100px; z-index: 99;
    display: flex; justify-content: space-between">
      <button class="btn-main" @click="goBack"><</button>
      <button class="btn-main" @click="goForvard">></button>
    </div>

    <my-start v-show="currentSlide === 1"></my-start>
    <my-sky v-show="currentSlide === 2"></my-sky>
    <my-people v-show="currentSlide === 3"></my-people>
    <my-ss v-show="currentSlide === 4"></my-ss>
    <my-sun v-show="currentSlide === 5"></my-sun>
    <my-ice v-show="currentSlide === 6"></my-ice>
    <my-end v-show="currentSlide === 7"></my-end>


  </div>
</template>

<script>
  import Start from './Start'
  import Sky from './Sky'
  import People from './people'
  import SS from './SS'
  import ice from './noSun'
  import Sun from './Sun'
  import End from './end'
export default {
  name: 'app',
  data () {
    return {
      currentSlide: 1
    }
  },
  components: {
    myStart: Start,
    mySky: Sky,
    myPeople: People,
    mySs: SS,
    myIce: ice,
    mySun: Sun,
    myEnd: End,
  },
  methods: {
    onKeyPress(event){
      event.preventDefault();
      if(event.keyCode === 39){
       this.goForvard();
      }
      if(event.keyCode=== 37){
       this.goBack();
      }
    },
    goForvard(){
      this.currentSlide++;
      if(this.currentSlide > 7) {
        this.currentSlide = 1;
      }
    },
    goBack(){
      this.currentSlide--;
      if( this.currentSlide <= 1 ) {
        this.currentSlide = 7;
      }
    }
  },
  mounted: function() {
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
  background: rgba(255,255,255,.5);
  color: white;
  font-size: 40px;
  border: none;
}
.btn-main:hover,
.btn-main:focus,
.btn-main:active{
  background: rgba(255,255,255,.8);
  color: red;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

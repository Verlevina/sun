<template>
  <div id="app">
   <my-start v-if="currentSlide === 1"></my-start>
    <my-sky v-if="currentSlide === 2"></my-sky>
    <my-people v-if="currentSlide === 3"></my-people>
    <my-ss v-if="currentSlide === 4"></my-ss>
    <my-sun v-if="currentSlide === 5"></my-sun>
    <my-ice v-if="currentSlide === 6"></my-ice>
    <my-end v-if="currentSlide === 7"></my-end>
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
      console.log (event.keyCode);
      if(event.keyCode === 39){
        this.currentSlide++;
        if(this.currentSlide > 7) {
          this.currentSlide = 1;
        }
        console.log(this.currentSlide)
      }
      if(event.keyCode=== 37){
        this.currentSlide--;
        if( this.currentSlide <= 1 ) {
          this.currentSlide = 7;
        }
        console.log(this.currentSlide)
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

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

<template>
  <div id="people" class="people">
    <h2> Солнце и люди </h2>
  </div>
</template>


<script>
  export default {
    name: 'People',
    data () {
      return {}
    },
  }
</script>

<style>
  .people{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    width: 100%;
    height: 100%;
    background: black;
    background-image: url("./assets/people.jpg");
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;
    color: white;
  }

  .people h2 {
    font-size: 100px;
    padding: 40px;
    margin-top: 0;
    color: yellow;
  }
</style>

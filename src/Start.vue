<template>
  <div id="start" class="start">
    <h1> Доклад</h1>
    <p>Левитиной Жени</p>
    <h2>Солнце</h2>
  </div>
</template>


<script>
  export default {
    name: 'Start',
  }
</script>

<style>
  .start{
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100%;
    background: black;
    background-image: url("./assets/1.jpg");
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;
    color: white;
  }
  .start h1 {
    margin: 30px;
    font-size: 80px;
  }
  .start p {
    font-size: 40px;
    margin-top: 0;
    color: black
  }
  .start h2 {
    font-size: 140px;
    margin-top: 0;
    color: yellow;
  }

</style>

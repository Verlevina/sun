<template>
  <div id="ss" class="ss">
    <h2> Планеты </h2>
    <div class="ssGif"></div>
  </div>
</template>


<script>
  export default {
    name: 'SS',
  }
</script>

<style>
  .ss{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 100%;
    height: 100%;
    background: black;

    color: white;
  }
  .ssGif{
    width: 400px;
    height: 400px;
    background-image: url("./assets/ss.gif");
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;
  }

  .ss h2 {
    font-size: 100px;
    padding: 40px;
    margin-top: 0;
    color: yellow;
  }
</style>

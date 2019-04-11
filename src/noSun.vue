<template>
  <div id="ss" class="nosunn">
    <div>
      <h2> Свет </h2>
      <div class="photo light"></div>
    </div>
    <div>
      <h2> Тепло </h2>
      <div class="photo warm"></div>
    </div>
    <div>
    <h2> Без солнца </h2>
    <div class="photo earth"></div>
    </div>
  </div>
</template>


<script>
  export default {
    name: 'ice',
  }
</script>

<style>
  .nosunn{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    flex-wrap: wrap;
    align-items: center;
    width: 100%;
    height: 100%;
    background: black;
    color: white;
  }
  .photo {
    width: 400px;
    height: 400px;
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;

  }
  .light {
    background-image: url("./assets/light.jpg");
  }
  .warm {
    background-image: url("./assets/warm.jpg");
  }

  .earth{
    background-image: url("./assets/ice.jpg");
  }

  .ss h2 {
    font-size: 100px;
    padding: 40px;
    margin-top: 0;
    color: yellow;
  }
</style>

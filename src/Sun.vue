<template>
  <div class="sun">
    <div>
      <h2> Солнечные пятна </h2>
      <img src="./assets/Sundark.jpg" alt="">
      <img src="./assets/SunDark1.jpg" alt="">

    </div>
    <div>
      <h2> Солнечные вспышки </h2>
      <img src="./assets/sunLight.jpg" alt="">
      <img src="./assets/sunLight1.jpg" alt="">

    </div>
  </div>
</template>

<script>
export default {
  name: 'ice'
}
</script>

<style>
  .sun{
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
  .sun img {
    width: 300px;
    height: 200px;

  }

  .sun h2 {
    font-size: 50px;
    padding: 40px;
    margin-top: 0;
    color: yellow;
  }
</style>

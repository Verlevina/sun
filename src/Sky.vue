<template>
  <div id="sky" class="sky">
      <h2> Звезды </h2>
  </div>
</template>


<script>
  export default {
    name: 'Sky',
  }
</script>

<style>
  .sky{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-end;
    width: 100%;
    height: 100%;
    background: black;
    background-image: url("./assets/sky.jpg");
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;
    color: white;
  }

  .sky h2 {
    font-size: 100px;
    padding: 40px;
    margin-top: 0;
    color: yellow;
  }

</style>

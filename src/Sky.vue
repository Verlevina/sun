<template>
  <div
    id="sky"
    class="sky"
    v-bind:class = sheetParam.class
  >
      <h2   v-bind:class = "{left: sheetParam.left}"> {{sheetParam.title}} </h2>
    <p>{{sheetParam.url}}</p>
  </div>
</template>

<script>
export default {
  name: 'Sky',
  data () {
    return {
    }
  },
  props: ['sheetParam']
}
</script>

<style scoped>
  .sky{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-end;
    width: 100%;
    height: 100%;
    background: black;
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;
    color: white;
  }
  .people-url {
    background-image: url("./assets/people.jpg")
  }
  .sky-url {
    background-image: url("./assets/sky.jpg")
  }
  .left {
    align-self: flex-start;
  }

  .sky h2 {
    font-size: 100px;
    padding: 40px;
    margin-top: 0;
    color: yellow;
  }

</style>

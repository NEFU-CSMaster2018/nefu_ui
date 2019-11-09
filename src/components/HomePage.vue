<template>
  <div class="home-container">
    <div class="picture-wall"></div>
    <div class="introduction"></div>
    <div class="contanct-info"></div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home-container {
  height: 100%;
  width: 100%;
  background-image: url(../../assets/images/homepage/pagebg1.jpg);
  background-size: cover;
}
</style>

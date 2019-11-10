<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
div,ul,li,h3,p {
  margin: 0;
  padding: 0;
}
ul,li {
  list-style: none;
  text-decoration: none;
}
#app {
  font-size: 1em;
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}
</style>

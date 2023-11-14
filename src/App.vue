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
body{
  background-image: url("assets/page_bg.png");
  background-size: cover;
}
*{
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
}
</style>

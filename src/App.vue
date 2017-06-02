<template>
  <div id="app">
    <homePage></homePage>
  </div>
</template>

<script>
import Login from './components/Login'
import homePage from './components/homePage'

export default {
  name: 'app',
  components: {Login, homePage}
}
</script>

<style>
*{
  margin:0;
  padding:0;
}

html, body{
  /*height:144rem;
  width:81rem;*/
  height:100%;
  width:100%;
  overflow: hidden;
}

#app {
  height:100%;
  width:100%;
}
</style>

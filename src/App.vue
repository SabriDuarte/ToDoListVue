<template>
  <div id="app">
    <home></home>
  </div>
</template>

<script>

import Home from './views/Home'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
  body{
    width: 280px;
    height: 529px;
    border: 1px solid #333333;
    padding: 15px;
  }
  ul{
    width: 80%;
    padding: 0;
    margin: 0 auto;
    border: none;
    display: flex;
    justify-content: center;
  }
  li{
    list-style: none;
  }
</style>

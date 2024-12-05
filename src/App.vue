<script setup>
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
// import Test from './components/songinfo.vue'
// import Player from './components/mp3player.vue'
import Slide from './components/slide.vue'
import Controller from './components/RemoteCTNL.vue'

</script>

<template>
  <header>
    <controller/>

    <Slide id="slide-1"></Slide>
    <Slide id="slide-2"></Slide>
    <Slide id="slide-3"></Slide>


  </header>
</template>

<style scoped>
header{
  /* display: flex;
  align-items: start;
  justify-content: center;
  width: 100%; height: 100%;
  border: 1px solid white;
  box-sizing: border-box; */
}
</style>

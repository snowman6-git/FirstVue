<script setup>
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
// import Test from './components/songinfo.vue'
// import Player from './components/mp3player.vue'
import Slide from './components/SildePage.vue'
import Controller from './components/RemoteCTNL.vue'

</script>

<template>
  <header>
    <controller/>

    <Slide id="slide-1" class="center">
      <h1>여긴 1페이지입니다</h1>
      <br>
      <div>새로운걸 배우는건 항상 재밌네요</div>
    </Slide>

    <Slide id="slide-2">
      <h1>여긴 2페이지입니다</h1>
      <div>slot을 쓰면 컴포넌트안에 넣어도 html태그처럼 안에 쓸 수 있습니다</div>
    </Slide>

    <Slide id="slide-3" class="center">
      <h1>오늘해볼것은 무엇인가요?</h1>
      <div>오늘은 동적생성과 페이지 볼떄 애니메이션 터지는 기능을 만들거 같네요</div>
    </Slide>


  </header>
</template>

<style scoped>
.center{
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  flex-direction: column;
}
</style>



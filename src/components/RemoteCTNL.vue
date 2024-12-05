<script setup>
import { onMounted, onBeforeUnmount } from 'vue';

let now = 1

const Go = (pos) => {
  if (pos == "next" && document.querySelector(`#slide-${now+1}`)){now += 1} //다음 슬라이드가 있는지 확인 후 넘기기
  if (pos == "back" && document.querySelector(`#slide-${now-1}`)){now -= 1}
  window.location.href = `#slide-${now}` //뭐가 됐든 넘기기
};

const handleKeydown = (event) => {
  const keysToIgnore = ['ArrowRight', 'ArrowLeft', 'ArrowUp', 'ArrowDown', 'Enter']; //슬라이드 넘길키
  if (keysToIgnore.includes(event.key)) {
    event.preventDefault(); // 특정 키 무시
    if (event.key == "ArrowRight" || event.key == "ArrowDown"){Go("next")} //오른쪽 방향키 또는 아래면 넘기기
    if (event.key == "ArrowLeft" || event.key == "ArrowUp"){Go("back")}
  }
};

onMounted(() => {
  window.addEventListener('keydown', handleKeydown);
});
onBeforeUnmount(() => {
  window.removeEventListener('keydown', handleKeydown);
});
</script>

<template>
  <div></div>
</template>

<style>
#player{
  position: fixed;
}
</style>


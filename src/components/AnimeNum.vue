<script setup>
import { ref, reactive, watch } from 'vue'
import gsap from 'gsap'

const number = ref(0)
const tweened = reactive({
  number: 0
})
let test = 1000;
watch(
  number,
    gsap.to(tweened, { duration: 0.5, number: Number(test) || 0 })
)
</script>

<template>
  <div class="demo">
    벌써 <p class="big-number">{{ tweened.number.toFixed(0) }}</p>명이 사용중이에요!
  </div>
</template>

<style>
.big-number {
  font-weight: bold;
  font-size: 2em;
}
</style>

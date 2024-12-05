<script>
export default {
  name: 'SildePage',
};
</script>

<template>
  <div class="page">
    <slot></slot>
  </div>
</template>

<style>
.page{
  padding: 1rem;
  width: 100vw; height: 100vh;
  /* border: 1px solid white; */
  box-sizing: border-box;
}
</style>

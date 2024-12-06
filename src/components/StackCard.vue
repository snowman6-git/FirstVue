<script>
export default {
  name: 'SildePage',
};
</script>

<template>

  <div class="card">
    <slot></slot>
  </div>

</template>

<style>
.card{
  width: 12rem; height: 20rem;
  border: 3px solid black;
  position: fixed;
  box-sizing: border-box;
  background-color: white;
  transition: all 0.5s;

}
.card:hover{
  scale: 1.25;
  rotate: -30deg;
}
</style>

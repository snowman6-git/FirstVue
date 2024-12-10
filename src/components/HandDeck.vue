<template>
  <div id="hand">
    <slot></slot>
  </div>
</template>

<style>
#hand {
  bottom: 7rem;
  /* transform: rotate(-90deg); */
  /* right: -45vw; */
  position: fixed;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>

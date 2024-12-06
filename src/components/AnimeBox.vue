<template>
  <div>
    <div class="box" v-bind:class="{ visible: isVisible }">
      더 나은 무언가를 찾고있나요
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false,
    };
  },
  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          this.isVisible = true;  // 요소가 화면에 보일 때
          observer.unobserve(entry.target); // 더 이상 관찰하지 않음
        }
      });
    });

    const target = this.$el.querySelector('.box');
    observer.observe(target); // 박스를 관찰
  },
};
</script>

<style>
.box {
  width: 300px;
  height: 100px;
  background-color: lightblue;
  margin: 20px 0;
  opacity: 0;
  transition: opacity 0.5s ease;
}

.box.visible {
  opacity: 1;
}
</style>

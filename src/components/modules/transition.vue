<template>
  <div :class="{fadeIn: visible}">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class transitionComponent extends Vue {
  private visible = false
  private scrollY = 0
  // スクロール量取得
  private onScroll() {
    this.scrollY = window.scrollY;
  }

  created() {
      window.addEventListener("scroll", this.handleScroll);
    }

  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }

  private handleScroll() {
    if (!this.visible) {
      var top = this.$el.getBoundingClientRect().top;
      this.visible = top < window.innerHeight + 100;
    }
  }
}
</script>

<style scoped>
/* トランジション */
.fadeIn {
  animation: fadeIn 1.5s;
}
@keyframes fadeIn {
  0% 
  {
    opacity: 0;
    transform: translateY(100px);
  }
  100% 
  {
    opacity: 1;
    transform: translateY(0px);
  }
}
</style>

<template>
  <div>
    <b-navbar type="dark" class="navba" fixed="top" :variant="this.scrollY ? 'dark ' : ''">
      <!-- ナビ左側 -->
      <b-navbar-nav >
        <b-nav-item href="#">Top</b-nav-item>
        <b-nav-item href="#">Profile</b-nav-item>
        <b-nav-item href="#">Gallery</b-nav-item>
      </b-navbar-nav>
      <!-- ナビ右側 -->
      <b-navbar-nav  class="ml-auto">
        <b-nav-item href="https://twitter.com/37__chi">
          <b-icon icon="twitter" style="width: 20px; height: 20px;"/>
          Twitter
        </b-nav-item>
        <b-nav-item href="https://github.com/37-chi">
          <b-icon icon="github" style="width: 20px; height: 20px;"/>
          GitHub
        </b-nav-item>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class MainHeader extends Vue {
  private scrollY =0
  // スクロール量取得
  private onScroll() {
    this.scrollY = window.scrollY;
  }

  mounted() {
  window.addEventListener('scroll', this.onScroll);
  }
}
</script>

<style scoped>
.navba {
  color: rgb(0, 0, 0);
  border-color: transparent;
}
.navbar li {
  color: rgb(126, 68, 68);
  background-color: transparent;
  border-color: transparent; } 
  .wrapper {
  position: sticky;
  top: 0;
}
</style>

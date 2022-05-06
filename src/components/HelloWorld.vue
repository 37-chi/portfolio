<template>
  <div class="home">
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home{
  height: 100vh; /* 全画面表示 */
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  background-image: url(../assets/Home.jpg);
}
</style>

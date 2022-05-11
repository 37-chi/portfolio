<template>
  <div class="home">
    <p>PORTFOLIO</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Main extends Vue {
  @Prop() private msg!: string;
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100&display=swap');
.home{
  height: 100vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
}

.top-image{
  width: 100vh
}

p{
  font-family: 'Roboto', sans-serif;
  font-size:9vw;
  font-weight: 100;
  color: rgb(231, 230, 230);
  position: absolute;
  top:28vh;
  left:10vw;
  padding:0;
  margin:0;
}

/* スマホ用 */
@media screen and (max-width: 767px) {
  p{
    font-family: 'Roboto', sans-serif;
    font-size:14vw;
    font-weight: 100;
    color: rgb(231, 230, 230);
    position: absolute;
    top:30vh;
    left:10vw;
    padding:0;
    margin:0;
  }
}

</style>

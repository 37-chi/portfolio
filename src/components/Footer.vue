<template>
  <div class="home">
    <!-- Footer -->
    <b-container fluid class="p-4">
      <b-row class="justify-content-md-left">
        <b-col class="title">CONTACT</b-col>
        <!-- 迷惑メールが来ないようにメールアドレスは画像で表示する -->
      </b-row>
    </b-container>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Footer extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');

.home{
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  background: #e2e2e2;
  padding: 70px 0px 100px 0px;
}

.content{
  padding: 0px 0px 50px 0px;
}

.photo-right{
  width:700px;
}

.photo-left{
  width:700px;
  padding-top: 100px;
}

/* フォント */
/* セクションタイトル */
.title{
  font-family: 'Roboto', sans-serif;
  font-size: 2.5rem;
  font-weight: 100;
  color: rgb(15, 15, 15);
  padding: 0px 0px 75px 0px;
}

</style>

<template>
  <div class="home">
    <!-- Gallery -->
    <b-container fluid class="p-4">
      <b-row class="justify-content-md-left">
        <b-col class="title">Gallery</b-col>
      </b-row>
      <!-- スライダーでも良いかも(?) -->
      <b-row class="content justify-content-md-center">
        <b-col md="auto">
          <b-img class="photo-right" fluid :src="require('../assets/Gallery/IMG_1135.jpg')" alt="Image 1"></b-img>
        </b-col>
        <b-col md="auto">
          <b-img class="photo-left" fluid :src="require('../assets/Gallery/IMG_0553.jpg')" alt="Image 2"></b-img>
        </b-col>
      </b-row>
      <b-row class="content justify-content-md-center">
        <b-col md="auto">
          <b-img class="photo-right" fluid :src="require('../assets/Gallery/IMG_0663.jpg')" alt="Image 1"></b-img>
        </b-col>
        <b-col md="auto">
          <b-img class="photo-left" fluid :src="require('../assets/Gallery/IMG_1001.jpg')" alt="Image 2"></b-img>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Gallery extends Vue {
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
  background-image: url(../assets/Home.jpg);
  position: relative;
  padding: 70px 0px 100px 0px;
}

/* 画像を暗くするオーバーレイ */
.home::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.75);
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
  font-size: 4rem;
  font-weight: 100;
  color: rgb(231, 230, 230);
  padding: 0px 0px 90px 0px;
}

/* スマホ用 */
@media screen and (max-width: 767px) {
  .home{
    padding: 50px 0px 100px 0px;
  }

  .content{
    padding: 0px 0px 0px 0px;
  }

  .photo-right{
    width:auto;
    padding-top: 25px;
  }

  .photo-left{
    width:auto;
    padding-top: 25px;
  }

  /* フォント */
  /* セクションタイトル */
  .title{
    font-family: 'Roboto', sans-serif;
    font-size: 2.5rem;
    font-weight: 100;
    color: rgb(231, 230, 230);
    padding: 0px 0px 50px 0px;
  }
}

</style>

<template>
  <div class="home">
    <!-- 自己紹介文 -->
    <b-container  class="content">
      <!-- About -->
      <b-row class="justify-content-md-left inside-content">
        <!-- About 見出し -->
        <b-col cols="10" lg="2" class="title text-left">About</b-col>
        <!-- About 内容 -->
        <b-col class="pt-3">
          <b-row>
            <div class="icon-field">
              <img src="../assets/Icon.jpg" class="rounded-circle" width="80" height="80">
            </div>
            <b-col class="pl-10">
              <b-row>
                <b-col class="font-size text-left pt-2">KENGO TOSAKI</b-col>
              </b-row>
              <b-row>
                <b-col class="font-size text-left">engineer/web designer</b-col>
              </b-row>
            </b-col>
          </b-row>
          <b-row>
            <b-col class="text text-left pt-3">
              1995年生まれ。慶應義塾大学 文学部 美学美術史学専攻卒。
              2021よりベンチャー企業にてエンジニアとしてキャリアをスタート。
              高いキャッチアップ能力を買われ、業務ではフロントエンド、バックエンド、WEBデザイン等幅広い領域を担当。
              趣味は楽器演奏（ドラム・ギターベース）、旅行、写真・動画、運転（自動車・バイク）、キャンプ、映画・音楽鑑賞など。
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <!-- Skill -->
      <b-row class="justify-content-md-left inside-content">
        <!-- Skill 見出し -->
        <b-col cols="10" lg="2" class="title text-left">Skill</b-col>
        <!-- Skill 内容 -->
        <b-col class="pt-3">
          <b-row>
            <b-col class="pl-10">
              <b-row>
                <b-col class="font-size text-left">
                  Git, Vue, TypeScript, HTML, CSS, JS, Swift, SQL, Linux, Azure
                </b-col>
              </b-row>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <!-- Portfolio -->
      <b-row class="justify-content-md-left inside-content">
        <!-- Portfolio 見出し -->
        <b-col cols="11" lg="2" class="title text-left">Portfolio</b-col>
        <!-- Portfolio 内容 -->
        <b-col class="pt-3">
          <b-row>
            <b-col class="pl-10">
              <b-row>
                <b-col class="text text-left">
                  このポートフォリオはすべて自分で撮影した写真を使用して作成しました。
                  業務上でよく使用していたVueとTypeScriptの組み合わせで作成しています。
                  その他にはBootstrap-Vueを導入しています。
                  一旦形にする事に重点を置いて作成したのでアニメーション等をほぼ実装できていません。
                  今後はリッチなアニメーションを追加予定です。
                </b-col>
              </b-row>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
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
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');

.home{
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  background: #e6e6e6;
}

.content{
  padding: 100px 20px 100px 20px;
}

.inside-content{
  padding: 0px 0px 100px 0px;
}

.top-image{
  width: 100%;
}

.icon-field{
  width: 120px;
}

/* フォント */
/* セクションタイトル */
.title{
  font-family: 'Roboto', sans-serif;
  font-weight: 400;
  font-size: 2rem;
}

/* 強調したい部分 */
.font-size{
  font-family: 'Roboto', sans-serif;
  font-weight: 400;
  font-size: 1.2rem;
}

/* 本文等 */
.text{
  font-family: 'Roboto', sans-serif;
  font-weight: 300;
  font-size: 1rem;
}

</style>

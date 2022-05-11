<template>
  <div id="app">
    <!-- ヘッダー -->
    <MainHeader/>
    <!-- 本文ページにluxyで慣性スクロールを実装 -->
    <div id="luxy">
      <TopPage class="luxy-el parallax-bg" data-offset="0" data-speed-y="25" />
      <Profile class="luxy-el " data-offset="0"  data-speed-y="7"/>
      <Gallery class="luxy-el " data-offset="0" data-speed-y="1"/>
      <Footer class="luxy-el "  data-offset="0" data-speed-y="1"/>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import MainHeader from './components/modules/MainHeader.vue';
import TopPage from './components/TopPage.vue';
import Profile from './components/Profile.vue';
import Gallery from './components/Gallery.vue';
import Footer from './components/Footer.vue';
import luxy from 'luxy.js'


@Component({
  components: {
    MainHeader,
    TopPage,
    Profile,
    Gallery,
    Footer
  },
})
export default class App extends Vue {
  mounted(){
    // スマートフォンではluxyが上手く動かないのでロジックで制御
    if (navigator.userAgent.indexOf('iPhone') > 0 || navigator.userAgent.indexOf('Android') > 0 && navigator.userAgent.indexOf('Mobile') > 0 || navigator.userAgent.indexOf('iPad') > 0 || navigator.userAgent.indexOf('Android') > 0) {
      return 
    } else {
      luxy.init();
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.parallax-bg::before{
  content: "";
  background: url(assets/Home.jpg) no-repeat center center;
  background-size: cover;
  display: block;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: -1;
  transform: translateZ(0);
}

/* スマホ用 */
@media screen and (max-width: 767px) {
  .parallax-bg {
  }
  .parallax-bg::before{
    content: "";
    background: url(assets/Home.jpg) no-repeat center center;
    background-size: cover;
    display: block;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    z-index: -1;
    transform: translateZ(0);
  }
}

</style>

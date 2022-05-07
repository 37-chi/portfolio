<template>
  <div id="app">
    <!-- ヘッダー -->
    <MainHeader/>
    <!-- 本文ページにluxyで慣性スクロールを実装 -->
    <div id="luxy"> 
      <TopPage/>
      <Profile/>
      <Gallery/>
      <Footer/>
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
    luxy.init();
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


</style>

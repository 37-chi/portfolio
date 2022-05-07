<template>
  <div id="app">
    <MainHeader/>
    <Main/>
    <Profile/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Main from './components/Main.vue';
import Profile from './components/Profile.vue';
import MainHeader from './components/modules/MainHeader.vue';

@Component({
  components: {
    Main,
    Profile,
    MainHeader
  },
})
export default class App extends Vue {}
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

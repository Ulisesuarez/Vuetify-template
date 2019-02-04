<template>
  <v-app>
    <toolbar></toolbar>
    <v-content id="main">
      <router-view></router-view>
    </v-content>
    <simple-footer></simple-footer>
  </v-app>
</template>

<script>
import Toolbar from './components/Toolbar'
import SimpleFooter from './components/SimpleFooter'
export default {
  name: 'App',
  components: {
    Toolbar,
    SimpleFooter
  },
  data () {
    return {
      //
    }
  }
}
</script>
<style>
  @font-face {
    font-family: 'OpenSans';
    src: url('/assets/fonts/OpenSans-Regular.eot');
    src: url('/assets/fonts/OpenSans-Regular.woff') format('woff'), url('/assets/fonts/OpenSans-Regular.ttf') format('truetype'), url('/assets/fonts/OpenSans-Regular.svg') format('svg');
    font-weight: normal;
    font-style: normal;
  }
  @font-face {
    font-family: 'Play';
    src: url('/assets/fonts/Play-Regular.eot');
    src: url('/assets/fonts/Play-Regular.woff') format('woff'), url('/assets/fonts/Play-Regular.ttf') format('truetype'), url('/assets/fonts/Play-Regular.svg') format('svg');
    font-weight: normal;
    font-style: normal;
  }
  body {
    background-color: #fff;
    font-family: 'OpenSans','sans-serif';
    margin: 0;
  }
  img {
    border: 0;
  }
  #main{
    background-color: white;
  }
</style>

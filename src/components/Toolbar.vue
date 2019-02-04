<template>
  <v-toolbar height="130" id="toolbar" app>
    <v-btn flat href="/" id="logo">ZERO TYPE</v-btn>
    <v-spacer class="hidden-md-and-up"></v-spacer>
    <v-menu v-if="$vuetify.breakpoint.smAndDown" bottom left>
      <v-btn
        slot="activator"
        ligth
        icon
        large
      >
        <v-icon style="font-size: 40px !important;margin-right: 10vw">menu</v-icon>
      </v-btn>

      <v-list>
        <v-list-tile
          v-for="(button, i) in paths"
          :key="i"
          @click="goTo(button.href)"
        >
          <v-list-tile-title>{{ button.name }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-menu>
    <v-hover v-else v-for="(button, index) in paths">
    <v-btn
      slot-scope="{ hover }"
      @click="changeCurrent(index)"
      :class="button.current? 'current navButton text-capitalize': 'navButton text-capitalize'"
      :style="button.first? 'margin-left: 5vw;':''"
      flat
      :href="button.href"
      :color="hover ? '#000000' : '#818181'">{{button.name}}</v-btn>
      </v-hover>
  </v-toolbar>
</template>

<script>
export default {
  name: 'toolbar',
  data() {
    return {
      paths: [ {name:'Home', href: '/', first: true, current: false},
        {name:'Features', href: 'feature', current: false},
        {name:'News', href: 'news', current: false},
        {name:'About', href: 'about', current: false},
        {name:'Contact', href: 'contact', current: false}]
    }
  },
  mounted() {
    this.paths.forEach(button=>{
      if (this.$route.path.includes(button.href)|| (this.$route.name && this.$route.name.includes(button.href))){
        button.current = true
      } else { console.log(this.$route.path)}
    })
  },
  methods: {
    changeCurrent(index){
      this.paths.forEach(button => button.current = false)
      this.paths[index].current = true
    }
  }
}
</script>

<style>
  #toolbar #logo{
    margin-left: 15vw;
    background: url(../assets/images/logo.png) no-repeat center top;
    color: #000;
    display: block;
    font: 15px/30px 'Play';
    height: 20px;
    width: 76px;
    padding-top: 68px;
    text-decoration: none;
  }
  .v-btn--active:before,
  .v-btn:hover:before,
  .v-btn:focus:before,
  .v-btn:active:before{
    background-color: transparent!important;
  }
  .navButton{
    font-family: 'Play','serif';
    font-size: 1.2em;
    }

  .current{
    color: #F99634 !important;
  }

</style>

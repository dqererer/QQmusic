<template>
  <div id="app">
    <MusicHall v-if="curTab=='music'"/>
    <Found v-if="curTab=='found'"/>
    <Mine v-if="curTab=='mine'"/>
    <PlayBar/>
    <NavBar :curTab="curTab" :switchTab="switchTab"/>
  </div>
</template>

<script>
import Found from './components/Found.vue';
import Mine from './components/Mine.vue';
import MusicHall from './components/MusicHall/MusicHall.vue';
import NavBar from './components/NavBar.vue';
import PlayBar from './components/PlayBar.vue';
export default {
  name: 'app',
  components: {
    NavBar,
    PlayBar,
    MusicHall,
    Mine,
    Found
  },
  data() {
    return {
      curTab:"music"
    }
  },
  methods:{
    switchTab:function(str){
      this.curTab = str;
    },
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  /* margin-top: 60px; */
  height: 100px;
}
</style>

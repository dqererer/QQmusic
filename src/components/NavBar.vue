<template>
  <div class="NavBar">
    <div class="music" v-on:click="navMusic">
      <!-- <img v-if="curTab!='music'" v-bind:src="url_music_defult" alt="">
      <img v-if="curTab=='music'" v-bind:src="url_music_onclick" alt=""> -->

      <img v-bind:src="curTab !== 'music' ? url_music_defult : url_music_onclick" alt="">
    </div>
    <div class="found" v-on:click="navFound">
      <img v-if="curTab!='found'" v-bind:src="url_found_defult" alt="">
      <img v-if="curTab=='found'" v-bind:src="url_found_onclick" alt="">
    </div>
    <div class="mine" v-on:click="navMine">
      <img v-if="curTab!='mine'" v-bind:src="url_mine_defult" alt="">
      <img v-if="curTab=='mine'" v-bind:src="url_mine_onclick" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  props: {
    curTab:String,
    switchTab:Function
  },
  data() {
    return {
      url_music_defult: require("../assets/icon/nav_music_defult.png"),
      url_music_onclick: require("../assets/icon/nav_music_onclick.png"),
      url_found_defult: require("../assets/icon/nav_found_defult.png"),
      url_found_onclick: require("../assets/icon/nav_found_onclick.png"),
      url_mine_defult: require("../assets/icon/nav_mine_defult.png"),
      url_mine_onclick: require("../assets/icon/nav_mine_onclick.png")
    };
  },
  methods: {
    navMusic: function() {
      this.switchTab("music");
    },
    navFound: function() {
      this.switchTab("found");
    },
    navMine: function() {
      this.switchTab("mine");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.NavBar {
  position: fixed;
  bottom: 10px;
  border-top: 1px solid #dad1d1;
  width: 100%;
  padding-top: 4px;
  div {
    width: 42px;
    height: 42px;
    float: left;
    padding: 10px 40px;
    img {
      width: 100%;
    }
  }
}
</style>

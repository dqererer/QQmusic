<template>
  <div class="PlayBar">
    <div class="music_info">
      <img v-bind:src="music_info" alt="">
      <span>{{music_name}}-{{singer}}</span>
    </div>
    <div class="list">
      <img src="../assets/icon/list.png" alt="">
    </div>
    <div class="play_button">
      <img src="../assets/icon/play.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: "PlayBar",
  props: {},
  data() {
    return {
      music_info: require("../assets/icon/jd.jpg"),
      music_name: "红豆",
      singer: "王菲"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.PlayBar {
  height: 50px;
  width: 100%;
  position: fixed;
  bottom: 100px;
  padding: 0 20px;
  div {
    height: 100%;
  }
  .music_info {
    // width: 60px;
    line-height: 50px;
    float: left;
    img {
      height: 120%;
      display: block;
      float: left;
    }
    span {
      font-size: 20px;
      margin-left: 20px;
      display: block;
      float: left;
    }
  }
  .play_button {
    float: right;
    margin-right: 20px;
    img {
      margin-top: 20px;
      height: 80%;
    }
  }
  .list {
    float: right;
    margin-right: 48px;
    img {
      margin-top: 20px;
      height: 80%;
    }
  }
}
</style>

<template>
  <div class="MusicHall">
    <div class="top">
      <div class="title">
        <span>音乐馆</span>
      </div>
      <div class="search">
        <Search/>
      </div>
      <div class="guess">
        <Guess/>
      </div>
    </div>
    <div class="slide">
      <SlideShow/>
    </div>
    <div class="nav_list">
      <div class="nav_item">
        <div class="icon">
          <img src="../assets/icon/singer.jpg" alt="">
        </div>
        <div class="text">
          <span>歌手</span>
        </div>
      </div>
      <div class="nav_item">
        <div class="icon">
         <img src="../assets/icon/rank.jpg" alt="">
         </div>
         <div class="text">
          <span>排行</span>
        </div>
      </div>
      <div class="nav_item">
        <div class="icon">
         <img src="../assets/icon/class.jpg" alt="">
         </div>
         <div class="text">
          <span>分类歌单</span>
        </div>
      </div>
      <div class="nav_item">
        <div class="icon">
         <img src="../assets/icon/radio.jpg" alt="">
         </div>
         <div class="text">
          <span>电台</span>
         </div>
       </div>
       <div class="nav_item">
        <div class="icon">
          <img src="../assets/icon/all.jpg" alt="">
        </div>
        <div class="text">
          <span>一起听</span>
        </div>
      </div>
      <div class="nav_item">
        <div class="icon">
         <img src="../assets/icon/singer.jpg" alt="">
         </div>
         <div class="text">
          <span>歌手</span>
         </div>
      </div>
    </div>
  </div>
</template>

<script>
import Search from "./Search.vue";
import SlideShow from "./SlideShow.vue";
import Guess from "./Guess.vue";
export default {
  name: "MusicHall",
  props: {},
  components: {
    Search,
    Guess,
    SlideShow
  },
  data() {
    return {};
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
// 问问大鹅，跨页面用less
@import url('../css/common.less');
.MusicHall {
  // .title{
  //   .titleP;
  // }
  padding: 20px 16px;
  height: 40px;
  .top {
    height: 100%;
    width: 100%;
    .title {
      font-size: 20px;
      font-weight: bolder;
      float: left;
      line-height: 40px;
    }
    .search {
      float: left;
      line-height: top;
    }
    .guess {
      float: left;
    }
  }
  .slide {
    margin-top: 10px;
  }
  .nav_list {
    width: 100%;
    height: 110px;
    margin-top: 16px;
    .nav_item {
      float: left;
      width: 15%;
      margin-left: 2px;
      margin-right: 2px;
      .icon {
        width: 40%;
        margin: 0 auto;
        img {
          width: 100%;
        }
      }
      .text {
        text-align: center;
        span {
          font-size: 8px;
        }
      }
    }
  }
}
</style>

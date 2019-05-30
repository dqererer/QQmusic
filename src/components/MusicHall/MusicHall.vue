<template>
  <div class="MusicHall">
    <div class="content">
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
            <img src="../../assets/icon/singer.jpg" alt="">
          </div>
          <div class="text">
            <span>歌手</span>
          </div>
        </div>
        <div class="nav_item">
          <div class="icon">
            <img src="../../assets/icon/rank.jpg" alt="">
          </div>
          <div class="text">
            <span>排行</span>
          </div>
        </div>
        <div class="nav_item">
          <div class="icon">
            <img src="../../assets/icon/class.jpg" alt="">
          </div>
          <div class="text">
            <span>分类歌单</span>
          </div>
        </div>
        <div class="nav_item">
          <div class="icon">
            <img src="../../assets/icon/radio.jpg" alt="">
          </div>
          <div class="text">
            <span>电台</span>
          </div>
        </div>
        <div class="nav_item">
          <div class="icon">
            <img src="../../assets/icon/all.jpg" alt="">
          </div>
          <div class="text">
            <span>一起听</span>
          </div>
        </div>
        <div class="nav_item">
          <div class="icon">
            <img src="../../assets/icon/singer.jpg" alt="">
          </div>
          <div class="text">
            <span>歌手</span>
          </div>
        </div>
      </div>
      <div class="radio_zone">
        <div class="left">
          <img src="../../assets/bg/radio_face.jpg" alt="">
        </div>
        <div class="right">
          <div class="top">
            <div class="left"></div>
            <div class="right"></div>
          </div>
          <div class="bottom">
            <div class="left"></div>
            <div class="right"></div>
          </div>
        </div>
      </div>
      <div class="songSheet">
        <SongSheet/>
      </div>
    </div>
  </div>
</template>

<script>
import Search from "../Search.vue";
import SlideShow from "../SlideShow.vue";
import Guess from "../Guess.vue";
import SongSheet from "./SongSheet.vue";
export default {
  name: "MusicHall",
  props: {},
  components: {
    Search,
    Guess,
    SlideShow,
    SongSheet
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
@import url("../../css/common.less");
.MusicHall {
  background-color: #fbf0f0;
  // padding: 20px 16px;
  .content {
    width: 330px;
    margin: 0 auto;
    padding-bottom: 80px;
    .top {
      height: 40px;
      width: 100%;
      padding-top: 11px;
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
      width: 100%;
    }
    .nav_list {
      width: 100%;
      height: 36px;
      margin-top: 12px;
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
    .radio_zone {
      width: 100%;
      height: 110px;
      margin-top: 16px;
      .left {
        float: left;
        height: 100%;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 10px 0px 10px #888888;
        img {
          height: 100%;
        }
      }
      .right {
        float: left;
        margin-left: 20px;
        .top,
        .bottom {
          background-color: blue;
          border-radius: 8%;
          width: 196px;
          height: 48px;
        }
        .top {
          margin-bottom: 10px;
        }
      }
    }
    .songSheet {
      margin-top: 10px;
      width: 100%;
    }
  }
}
</style>

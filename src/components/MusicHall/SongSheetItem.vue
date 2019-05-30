<template>
  <div class="SongSheetItem" >
    <div class="top" v-bind:style="{'background-image':'url(' + SongSheetItem.bg_img + ')'}">
      <div class="play_num">
        <img src="../../assets/icon/play_num.png" alt="">
        <span>{{SongSheetItem.playNum}}</span>
      </div>
    </div>
    <div class="bottom">
      <span>{{SongSheetItem.title}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "SongSheetItem",
  props: {
    SongSheetItem: Object
  },
  components: {},
  data() {
    return {};
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.SongSheetItem {
  height: 120px;
  width: 100px;
  .top {
    height: 100px;
    width: 100%;
    position: relative;
    border-radius: 8px;
    .play_num {
      position: absolute;
      left: 34px;
      top: 70px;
      width: 60px;
      height: 20px;
      background-color: gray;
      border-radius: 8px;
      img {
        margin-left: 5px;
        height: 80%;
      }
      span{
        color: white;
      }
    }
  }
}
</style>

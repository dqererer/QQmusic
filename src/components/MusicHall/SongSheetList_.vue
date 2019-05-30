<template>
  <div class="SongSheetList">
    <div class="top">
      <div class="SongSheetItem" v-for="(songItem,index) in songItems" v-bind:key=index>
        <SongSheetItem :songItem="songItem"/>
      </div>
    </div>
    <div class="bottom">

    </div>
  </div>
</template>

<script>
import SongSheetItem from "./SongSheetItem.vue";
export default {
  name: "SongSheetList",
  props: {},
  data() {
    return {
      songItems: [
        {
          bg_img: require("../../assets/bg/radio_face.jpg"),
          playNum: 1110,
          title: "哈哈哈哈哈"
        },
        {
          bg_img: require("../../assets/bg/radio_face.jpg"),
          playNum: 2220,
          title: "这是2222222"
        },
        {
          bg_img: require("../../assets/bg/radio_face.jpg"),
          playNum: 3330,
          title: "这是3333333"
        }
      ]
    };
  },
  components: {
    SongSheetItem
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.SongSheetList {
  height: 120px;
  .SongSheetItem {
    float: left;
    height: 120px;
    margin-right: 5px;
  }
}
</style>

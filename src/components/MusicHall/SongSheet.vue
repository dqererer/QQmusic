<template>
  <div class="SongSheet">
    <div class="top">
      <TopInfo :title="title"/>
    </div>
    <div class="SongSheetList">
      <SongSheetList :swiperSlides="swiperSlides_top"/>
    </div>
    <div class="SongSheetList">
      <SongSheetList :swiperSlides="swiperSlides_bottom"/>
    </div>
  </div>
</template>

<script>
import TopInfo from "./TopInfo.vue";
import SongSheetList from "./SongSheetList.vue";
export default {
  name: "SongSheet",
  props: {},
  components: {
    TopInfo,
    SongSheetList
  },
  data() {
    return {
      title: "为你推荐歌单",
      swiperSlides_top: [
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
        },
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
      ],
      swiperSlides_bottom: [
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
        },
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
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.SongSheet {
  .top {
    margin-top: 10px;
  }
}
</style>

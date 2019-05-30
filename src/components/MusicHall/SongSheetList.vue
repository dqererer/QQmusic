<template>
  <div class="SongSheetList">
    <swiper :options="swiperOption">
      <swiper-slide class="SongSheetItem" v-for="(slide, index) in swiperSlides" :key="index">
        <SongSheetItem :songItem="slide"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
import SongSheetItem from "./SongSheetItem.vue";
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  name: "SongSheetList",
  data() {
    return {
      swiperOption: {
        slidesPerView: 3,
        slidesPerGroup: 3,
        
        pagination: {
          el: ".swiper-pagination"
        }
      },
      swiperSlides: [
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
  components: {
    SongSheetItem,
    swiper,
    swiperSlide
  }
  // mounted() {
  //   setInterval(() => {
  //     console.log("simulate async data");
  //     if (this.songItems.length < 10) {
  //       this.songItems.push(this.songItems.length + 1);
  //     }
  //   }, 3000);
  // }
};
</script>

<style scoped lang="less">
.SongSheetList {
  height: 120px;
  width: 100%;
  .SongSheetItem {
    float: left;
    height: 120px;
    margin-right: 12px;
  }
}
</style>
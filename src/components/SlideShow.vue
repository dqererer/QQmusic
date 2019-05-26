<template>
  <div class="SlideShow">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(slide, index) in swiperSlides" :key="index" v-bind:style="{'background-image':'url(' + slide.imgUrl + ')'}"></swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>  
</template>

<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  name: "SlideShow",
  components: {
    swiper,
    swiperSlide
  },
  data() {
    return {
      swiperOption: {
        autoplay: {
          delay: 3000,
          disableOnInteraction: false
        },
        loop: true,
        pagination: {
          el: ".swiper-pagination"
        }
      },
      swiperSlides: [
        { imgUrl: require("../assets/bg/slide1.jpg") },
        { imgUrl: require("../assets/bg/slide2.jpg") },
        { imgUrl: require("../assets/bg/slide3.jpg") }
      ]
    };
  },
  mounted() {
    // setInterval(() => {
    //   console.log("simulate async data");
    //   if (this.swiperSlides.length < 10) {
    //     this.swiperSlides.push(this.swiperSlides.length + 1);
    //   }
    // }, 3000);
  }
};
</script>

<style scoped lang="less">
.SlideShow {
  height: 170px;
  width: 330px;
  position: relative;
  .swiper-container,
  .swiper-wrapper {
    width: 100%;
    height: 100%;
    .swiper-slide {
      width: 100%;
      height: 100%;
      display: block;
      background-repeat: no-repeat;
      background-size: 100% 100%;
    }
  }

  .swiper-pagination {
    /deep/ .swiper-pagination-bullet {
      background: #736e6e;
      border:solid 1px red;
      background: blue;
    }
    /deep/ .swiper-pagination-bullet-active {
      background: white;
    }
  }
}

</style>

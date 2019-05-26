<template>
  <div class="SlideShow_">
    <!-- <div class="slide_list">
      <a v-for="(slide,index) in slides" class="slide_item" v-bind:key=index v-bind:style="{'background-image':'url(' + slide.imgUrl + ')'}"></a>
    </div> -->
    <!-- 考过来的 -->
     <swiper>
    <!-- slides -->
    <swiper-slide>I'm Slide 1</swiper-slide>
    <swiper-slide>I'm Slide 2</swiper-slide>
    <swiper-slide>I'm Slide 3</swiper-slide>
    <swiper-slide>I'm Slide 4</swiper-slide>
    <swiper-slide>I'm Slide 5</swiper-slide>
    <swiper-slide>I'm Slide 6</swiper-slide>
    <swiper-slide>I'm Slide 7</swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
    <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div>
    <div class="swiper-scrollbar"   slot="scrollbar"></div>
  </swiper>
  <!-- 考过来的 -->
    <!-- <div class="slide_nav">
      <div class="slide_nav_item slide_nav_current"></div>
      <div class="slide_nav_item"></div>
      <div class="slide_nav_item"></div>
    </div> -->
  </div>
</template>


<script>
// import '../dist/swiper.min.js'
import 'swiper/dist/css/swiper.css'

import { swiper, swiperSlide } from 'vue-awesome-swiper'

export default {
  name: "SlideShow_",
  props: {},
  components: {
    swiper,
    swiperSlide
  },
  data() {
    return {
      slides: [
        {
          // isShow: true,
          imgUrl: require("../assets/bg/slide1.jpg")
        },
        {
          // isShow: true,
          imgUrl: require("../assets/bg/slide2.jpg")
        },
        {
          // isShow: true,
          imgUrl: require("../assets/bg/slide3.jpg")
        }
      ]
    };
  },
  methods: {
    slide: function() {
      var item_length = this.slides.length;
      var close = setInterval(function() {
        for (var i = 0; i < item_length; i++) {
          document.getElementsByClassName("slide_item")[i].style.transform =
            "translateX(-200px)";
        }
      }, 100);
    }
  },
  created: function() {
    // this.slide();

    var mySwiper = new Swiper(".swiper-container", {
      direction: "vertical", // 垂直切换选项
      loop: true, // 循环模式选项

      // 如果需要分页器
      pagination: {
        el: ".swiper-pagination"
      },

      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },

      // 如果需要滚动条
      scrollbar: {
        el: ".swiper-scrollbar"
      }
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
@import url("../dist/swiper.min.css");

.SlideShow {
  height: 170px;
  width: 330px;
  position: relative;
  .slide_list {
    width: 10000%;
    height: 100%;
    .slide_item {
      width: 1%;
      height: 100%;
      display: block;
      background-repeat: no-repeat;
      background-size: 100% 100%;
      float: left;
      margin-right: 20px;
      animation: myslide 5s infinite;
    }

    @keyframes mymove {
      from {
        left: 0px;
      }
      to {
        left: 200px;
      }
    }
  }
  .slide_nav {
    position: absolute;
    top: 144px;
    left: 134px;
    .slide_nav_item {
      display: block;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: #736e6e;
      float: left;
      margin-right: 10px;
    }
    .slide_nav_current {
      background: white;
    }
  }
}
</style>

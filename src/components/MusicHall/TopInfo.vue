<template>
  <div class="TopInfo">
    <div class="left">
      <span>{{title}}</span>  
    </div>
    <div class="right">
      <span>更多></span>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopInfo",
  props: {
    title: String
  },
  data() {
    return {};
  },
  methods: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.TopInfo {
  width: 100%;
  height: 30px;
  padding: 0px 0px;
  line-height: 30px;
  .left {
    float: left;
    font-size: 18px;
    color: black;
    font-weight: bold;
  }
  .right {
    float: right;
    font-size: 12px;
  }
}
</style>

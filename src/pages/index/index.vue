<template>
  <view class="index">
    <h3>路由模式为 browser, 无法获取路由参数</h3>
    <button @click="gotoModel">goto model page</button>
  </view>
</template>

<script>
import Taro from "@tarojs/taro";

export default {
  name: "Index",
  components: {},
  setup() {
    const gotoModel = () => {
      Taro.navigateTo({
        url: "/pages/model/model?mid=8",
      });
    };

    return {
      gotoModel,
    };
  },
};
</script>

<style>
.index {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

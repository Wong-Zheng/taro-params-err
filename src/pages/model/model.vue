<template>
  <view class="model">
    <h1>mid: {{ mid }}</h1>
  </view>
</template>

<script>
import { onMounted, ref } from "vue";
import Taro from "@tarojs/taro";

export default {
  name: "Model",
  components: {},
  setup() {
    let mid = ref("");

    onMounted(() => {
      mid.value = Taro.getCurrentInstance().router.params.mid;
      console.log("onMounted---params", mid.value);
    });

    return {
      mid,
    };
  },
};
</script>

<style>
.model {
}
</style>

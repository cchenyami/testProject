<template>
  <div class="login">
    <h1 class="animate__animated animate__bounce">An animated element</h1>

    <div class="element">23r23r2r23r测试啊啊啊啊啊</div>
  </div>
</template>

<script lang="ts" setup>
import Typed from 'typed.js';
import { nextTick, onMounted } from 'vue';



// var typed = new Typed('.element', {
//   strings: ["First sentence.", "Second sentence."],
//   typeSpeed: 30
// });

function init() {
  nextTick(() => {
   var typed = new Typed(".element", {
  // 键入“first”后等待1000毫秒
  strings: ["First ^1000 sentence.", "Second sentence."]
});

  })
}
onMounted(init)
</script>

<style lang="less">
.login {
  width: 100%;
  height: 100%;
}
</style>
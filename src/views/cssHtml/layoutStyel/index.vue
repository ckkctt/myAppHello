<template>
  <div class="container">
    <div class="left"></div>
    <div class="right"></div>
  </div>
</template>

<style scoped lang="less">
.container {
  height: 600px;
  width: 100%;
  min-width: 300px;
  .left {
    width: 35%;
    height: 100%;
    background: #ff0;
    float: left;
  }
  .right {
    overflow: hidden;
    width: 65%;
    height: 100%;
    background: #0f0;
  }
}
</style>

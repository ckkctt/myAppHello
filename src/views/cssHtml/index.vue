<template>
  <div class="vueStyelWarp">
    <div>
      <section @click="clickChange('CssStyel')">常见的css形状</section>
      <section @click="clickChange('LayoutStyel')">宽度自适应布局</section>
    </div>

    <!-- 组件传值 -->
    <div class="compontentStyle">
      <!--     动态组件 -->
      <keep-alive>
        <component :is="activeName" />
      </keep-alive>
    </div>
  </div>
</template>

<script>
import CssStyel from './cssStyel/index'
import LayoutStyel from './layoutStyel/index'
export default {
  components: {
    CssStyel,
    LayoutStyel
  },
  data () {
    return {
      activeName: 'CssStyel'
    }
  },
  methods: {
    clickChange (val) {
      this.activeName = val
    }
  }
}
</script>

<style scoped lang="less">
.vueStyelWarp {
  height: 100%;
  width: 100%;
  position: relative;
  padding: 20px;
  section {
    color: rgb(86, 151, 21);
    cursor: pointer;
    margin-top: 10px;
  }
  section:hover {
    color: #13eb7f;
  }
  .compontentStyle {
    margin-left: 100px;
    position: absolute;
    top: 30px;
    left: 30px;
  }
}
</style>

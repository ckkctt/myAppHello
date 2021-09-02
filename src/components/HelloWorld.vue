<template>
  <div class="styelWarp">
    <div class="styelWarpTop">
      <section @click="clickChange('vue')">vue</section>
      <section @click="clickChange('react')">react</section>
      <section @click="clickChange('javaScript')">javaScript</section>
      <section @click="clickChange('elementUi')">elementUi</section>
      <section @click="clickChange('cssHtml')">cssHtml</section>
    </div>

    <!-- 组件传值 -->
    <div>
      <!--     动态组件 -->
      <keep-alive>
        <component :is="activeName" />
      </keep-alive>
    </div>
  </div>
</template>

<script>
import VUE from '../views/vue/index.vue'
import REACT from '../views/react/index.vue'
import JAVASCRIPT from '../views/javaScript/index.vue'
import ELEMENTUI from '../views/elementUi/index.vue'
import CSSHTML from '../views/cssHtml/index.vue'
export default {
  components: {
    VUE,
    REACT,
    JAVASCRIPT,
    CSSHTML,
    ELEMENTUI
  },
  data () {
    return {
      activeName: 'VUE'
    }
  },
  methods: {
    clickChange (val) {
      this.activeName = val
    }
  }
}
</script>

<style scoped>
.styelWarp {
  width: 100%;
}
.styelWarpTop {
  display: flex;
  justify-content: flex-start;
}
section{
    margin-left: 20px;
  }
</style>

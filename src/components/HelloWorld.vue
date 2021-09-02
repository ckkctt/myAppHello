<template>
  <div class="styelWarp">
    <div class="styelWarpTop">
      <section
        @click="clickChange('VUE')"
        :class="activeName === 'VUE' ? 'clickStyel' : ''"
      >
        vue
      </section>
      <section
        @click="clickChange('REACT')"
        :class="activeName === 'REACT' ? 'clickStyel' : ''"
      >
        react
      </section>
      <section
        @click="clickChange('JAVASCRIPT')"
        :class="activeName === 'JAVASCRIPT' ? 'clickStyel' : ''"
      >
        javaScript
      </section>
      <section
        @click="clickChange('ELEMENTUI')"
        :class="activeName === 'ELEMENTUI' ? 'clickStyel' : ''"
      >
        elementUi
      </section>
      <section
        @click="clickChange('CSSHTML')"
        :class="activeName === 'CSSHTML' ? 'clickStyel' : ''"
      >
        cssHtml
      </section>
    </div>

    <!-- 组件传值 -->
    <div class="styelWarpBottom">
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
      activeName: 'VUE',
      clickStyel: ''
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
.styelWarp {
  .styelWarpTop {
    display: flex;
    justify-content: flex-start;
    background: rgb(240, 229, 229);
    height: 50px;
    line-height: 50px;
    section {
      margin-left: 20px;
      cursor: pointer;
    }
    .clickStyel {
       color: #1890ff;
    }
  }
  .styelWarpBottom {
    margin-top: 20px;
    margin-left: 20px;
  }
}
</style>

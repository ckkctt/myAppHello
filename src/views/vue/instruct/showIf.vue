<template>
  <div>
      <el-button @click="change">
          点击渲染
      </el-button>
      <div v-if="showHide">
          {{name1}}
      </div>
      <div v-show="showHide">
          {{name2}}
      </div>
      <div :style="!showHide?'display:none':''">
          {{name3}}
      </div>
      <div :style="!showHide?'visibility:hidden':''">
          {{name4}}
          <span :style="!showHide?'visibility:visible':''"
            style="color:#0f0"
          >
              {{name5}}
          </span>
      </div>
      <div>
        {{111}}
      </div>
  </div>
</template>

<script>

export default {

  data () {
    return {
      name1: '我是渲染元素v-if',
      name2: '我是渲染元素v-show',
      name3: '我是渲染元素display:none',
      name4: '我是渲染元素visibility:hidden',
      name5: '我是渲染元素visibility:hidden的子元素',
      showHide: false
    }
  },
  methods: {
    change () {
      this.showHide = !this.showHide
    }
  }
}
</script>

<style scoped>

</style>

<template>
  <div class="box">
    {{ msg }}
    <!-- 动态组件 -->
    <div style="margin-left:100px">
      <el-button @click="change('OneSon')">
        组件1
      </el-button>
      <el-button @click="change('TwoSon')">
        组件2
      </el-button>
    </div>
    <!-- 缓存组件 -->
    <div>
      <keep-alive>
        <compontent :is="show" />
      </keep-alive>
    </div>
  </div>
</template>

<script>
import OneSon from './oneSon.vue'
import TwoSon from './twoSon.vue'
export default {
  components: {
    OneSon,
    TwoSon
  },
  data () {
    return {
      msg: 'father',
      show: ''
    }
  },
  created () {},
  methods: {
    change (val) {
      this.show = val
    }
  },
  activated () {
    console.log('我是父组件的activated')
  },
  deactivated () {
    console.log('我是父组件的deactivated')
  }
}
</script>

<style scoped>
.box {
  width: 560px;
  height: 300px;
  padding: 10px;
  border: 1px solid rgb(56, 148, 56);
  margin: 10px;
}
</style>

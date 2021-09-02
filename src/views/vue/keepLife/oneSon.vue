<template>
  <div class="box">
    <div style="margin:10px;">{{ msg }}</div>
    <div>{{ name }}</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'oneSon',
      name: '我是data存储的数据'
    }
  },
  activated () {
    console.log('我是子组件oneSon的activated')
  },
  deactivated () {
    console.log('我是子组件oneSon的deactivated')
  },
  mounted () {
    console.log(this.name)
  },
  created () {
    console.log(this.name)
  }
}
</script>

<style scoped>
.box {
  width: 200px;
  height: 180px;
  border: 1px solid rgb(49, 51, 160);
  margin: 20px;
}
</style>

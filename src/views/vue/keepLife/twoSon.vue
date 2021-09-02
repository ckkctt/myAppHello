<template>
    <div class="box">
        <div style="margin:10px;">{{msg}}</div>

    </div>
</template>

<script>
export default {

  data () {
    return {
      msg: 'twoSon'
    }
  },
  activated () {
    console.log('我是子组件twoSon的activated')
  },
  deactivated () {
    console.log('我是子组件twoSon的deactivated')
  }
}
</script>

<style scoped>
    .box{
        width: 200px;
        height: 180px;
        border: 1px solid rgb(49, 51, 160);
        margin:20px;
    }
</style>

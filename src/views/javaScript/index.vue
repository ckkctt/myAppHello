<template>
  <div>
    <div>{{ a.b }}</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      a: {}
    }
  },
  created () {
    this.a.b = 1
  },
  mounted () {
    this.a.b = 2
  }
}
</script>

<style scoped></style>

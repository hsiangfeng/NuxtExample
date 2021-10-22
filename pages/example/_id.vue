<template>
  <div>
    動態路由
  </div>
</template>

<script>
export default {
  created () {
    alert(this.$route.params.id)
  }
}
</script>

<style>

</style>

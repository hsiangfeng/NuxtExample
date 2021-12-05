<template>
  <div>
    這是 header
    <nuxt />
    這是 footer
  </div>
</template>

<script>
export default {
  middleware () {
    console.log('Layout middleware')
  }
}
</script>

<style>

</style>

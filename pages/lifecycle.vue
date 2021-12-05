<template>
  <div>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. In veritatis qui aut minima, architecto aliquid id. Repellat tempore vel beatae error neque quaerat incidunt quidem eum, facere doloremque, libero sint?
    <ul>
      <li v-for="item in users" :key="item.email">
        {{ item.email }}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  nuxtServerInit (store, content) {
    console.log('nuxtServerInit')
  },
  middleware () {
    console.log('Page middleware')
  },
  validate () {
    console.log('validate')
    return true
  },
  // async asyncData ({ $axios }) {
  //   const res = await $axios.get('https://randomuser.me/api/')

  //   return {
  //     data: res.data.results
  //   }
  // },
  data () {
    return {
      users: []
    }
  },
  async fetch () {
    const res = await this.$axios.get('https://randomuser.me/api/')
    this.users = res.data.results
  },
  beforeCreate () {
    console.log('beforeCreate')
  },
  created () {
    console.log('created')
  }
}
</script>

<style>

</style>

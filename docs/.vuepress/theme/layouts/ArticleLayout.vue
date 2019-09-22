<template lang="pug">
.theme-container
  Navbar
  .content-container
    h1 {{ $page.title }}
    Content
</template>

<script>
import Navbar from '../components/Navbar'

export default {
  components: {
    Navbar
  },
  mounted() {
    console.log(this.$site)
  }
}
</script>

<style lang="stylus">
.content-container
  padding 40px
  color $secondary-color
  background-color $secondary-background
</style>

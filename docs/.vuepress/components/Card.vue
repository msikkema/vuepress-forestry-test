<template lang="pug">
  .card-container(
    @click="go"
  ) {{ title }}
</template>

<script>
export default {
  props: {
    image: String,
    title: String,
    subTitle: String,
    link: String
  },
  methods: {
    go() {
      window.location.href = this.link
    }
  }
}
</script>

<style lang="stylus">
  .card-container
    height 400px
    width 250px
    background-color $secondary-background
    color $secondary-color

    &:hover
      cursor pointer
</style>

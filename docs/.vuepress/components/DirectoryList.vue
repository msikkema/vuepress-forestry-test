<template lang="pug">
  ul
    li(v-for="page in pages" :key="page[displayProp]")
      a(:href="page.path") {{ page[displayProp] }}
</template>

<script>
export default {
  props: {
    path: String,
    displayProp: String
  },
  computed: {
    pages() {
      return this.$site.pages.filter(p => p.path.indexOf(this.path) >= 0)
    }
  }
}
</script>

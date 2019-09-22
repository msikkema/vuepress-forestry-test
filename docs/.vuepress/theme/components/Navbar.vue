<template lang="pug">
  .navbar-container
    .logo-container
      img.logo(src="/reachout_logo.svg" @click="go('/')")
    .link-container
</template>

<script>

export default {
  props: {
    showHome: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    go: url => window.location.href = url
  }
}
</script>

<style lang="scss">
  .navbar-container {
    height: 70px;
    background-color: #0073CF;
    border-bottom: 2px solid white;
    display: flex;
    justify-content: space-between;
    margin-bottom: 15px;

    .logo-container {
      display: flex;
      align-items: center;

      img {
        cursor: pointer;
      }
    }
    .logo {
      height: 50px;
    }
    .link-container {
      display: flex;
      align-items: center;

      .navbar-link {
        font-size: 24px;
      }
    }
  }
</style>
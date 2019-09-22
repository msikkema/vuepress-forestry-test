<template lang="pug">
  .homepage-container
    h1 VuePress & Forestry.io test for ReachOut Australia

    h2 Articles
    .article-cards
      Card(
        class="card"
        v-for="page in $site.pages.filter(p => p.path.indexOf('/articles/') >= 0)"
        :key="page.title"
        :title="page.title"
        :link="page.path"
      )
</template>

<style lang="stylus">
  .article-cards
    display flex
    
    .card
      margin 5px
</style>

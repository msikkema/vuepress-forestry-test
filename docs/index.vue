<template lang="pug">
  .homepage-container
    h1 VuePress & Forestry.io test for ReachOut Australia

    h2 Articles
    div.article-cards(:class="articleCards")
      Card(
        :class="cardClasses"
        v-for="page in $site.pages.filter(p => p.path.indexOf('/articles/') >= 0)"
        :key="page.title"
        :title="page.title"
        :link="page.path"
        :image="page.frontmatter.heroImage"
        :sub-title="page.frontmatter.subtitle"
      )
</template>

<script>
import { css } from 'emotion'

const articleCards = css`display: flex;`;
const cardClasses = css`margin: 5px;`

export default {
  data() {
    return {
      articleCards,
      cardClasses
    }
  },
  mounted() {
    console.log(this.$site.pages.filter(p => p.path.indexOf('/articles/') >= 0))
  }
}
</script>

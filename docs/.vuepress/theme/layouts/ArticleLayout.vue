<template lang="pug">
.theme-container
  Navbar
  div(:class="contentContainer")
    h1 {{ $page.title }}
    Content
</template>

<script>
import { css } from 'emotion'
import Navbar from '../components/Navbar'
import { theme } from '../styles/palette.style'


const { colors: { secondaryColor, secondaryBackground } } = theme
const contentContainer = css`
  padding: 40px;
  color: ${secondaryColor};
  background-color: ${secondaryBackground};
`;

export default {
  components: {
    Navbar
  },
  data() {
    return {
      contentContainer
    }
  },
  mounted() {
    console.log(this.$site)
  }
}
</script>

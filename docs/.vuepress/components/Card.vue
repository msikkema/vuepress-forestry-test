<template lang="pug">
  div(:class="cardContainer" @click="go")
    div(:class="imageContainer(image)")
    div(:class="titleContainer")
      div(:class="cx(textPadding, titleClass)") {{ title }}
      div(:class="textPadding") {{ subTitle }}
</template>

<script>
import { css, cx } from 'emotion'
import { theme } from '../theme/styles/palette.style'

const {
  colors: {
    secondaryColor,
    secondaryBackground,
    primaryBackground
  }
} = theme

const textPadding = css`padding: 15px;`;

const titleClass = css`
  color: ${primaryBackground};
  font-size: 24px;
  margin-bottom: 20px;
`;

const cardContainer = css`
  height: 600px;
  width: 350px;
  flex-grow: 0;
  flex-shrink: 0;
  color: ${secondaryColor};
  overflow: hidden;
  border: 1px solid grey;

  &:hover { cursor: pointer; }
`;

const imageContainer = image => css`
  background-image: url(${image});
  background-size: cover;
  background-position: center;
  height: 50%;
`;

const titleContainer = css`
  height: 50%;
  background-color: ${secondaryBackground};
  color: ${secondaryColor};
`;

export default {
  data() {
    return {
      cardContainer,
      titleContainer,
      titleClass,
      textPadding
    }
  },
  props: {
    image: String,
    title: String,
    subTitle: String,
    link: String
  },
  methods: {
    go() {
      window.location.href = this.link
    },
    imageContainer,
    cx
  }
}
</script>

<template lang="pug">
  div(:class="navbarContainer")
    div(:class="logoContainer")
      img(:class="cx(logo, img)" src="/reachout_logo.svg" @click="go('/')")
    div(:class="linkContainer")
</template>

<script>
import { css, cx } from "emotion";

const linkContainer = css`
  display: flex;
  align-items: center;
`;

const logo = css`
  height: 50px;
`;

const img = css`
  cursor: pointer;
`;

const logoContainer = css`
  display: flex;
  align-items: center;
`;

const navbarContainer = css`
  height: 70px;
  background-color: #0073cf;
  border-bottom: 2px solid white;
  display: flex;
  justify-content: space-between;
  margin-bottom: 15px;
`;

export default {
  props: {
    showHome: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      navbarContainer,
      logoContainer,
      logo,
      img,
      linkContainer
    }
  },
  methods: {
    go: url => (window.location.href = url),
    cx
  }
};
</script>

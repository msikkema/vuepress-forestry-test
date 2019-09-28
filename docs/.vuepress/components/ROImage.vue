<template lang="pug">
  img(v-bind="$attrs" v-on="$listeners" :src="url")
</template>

<script>
export default {
  props: {
    url: String
  }
}
</script>

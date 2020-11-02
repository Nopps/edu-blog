<template>
  <footer>
    {{ text }}
  </footer>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: '',
    },
  },
}
</script>

<style>
footer {
  margin: 1rem auto !important;
  color: gray;
}
</style>

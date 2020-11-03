<template>
  <span class="tag"
    ><a :href="href">{{ text }}</a></span
  >
</template>

<script>
export default {
  props: {
    href: { type: String, default: '' },
    text: { type: String, default: '' },
  },
}
</script>

<style>
.tag a {
  box-shadow: none;
  color: #333333;
  font-size: 0.9rem;
  background-color: #e8eaec;
  border-radius: 5px;
  padding: 0.05rem 0.6rem 0.2rem 0.6rem;
}

.tag a:hover {
  background-color: #5aabf4;
  box-shadow: inset 0 -3px 0 rgba(44, 49, 63, 0.15);
}
</style>

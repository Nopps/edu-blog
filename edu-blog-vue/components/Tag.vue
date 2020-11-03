<template>
  <a class="tag" :href="url">{{ text }}</a>
</template>

<script>
export default {
  props: {
    url: { type: String, default: '#' },
    text: { type: String, default: '' },
  },
}
</script>

<style>
a.tag {
  box-shadow: none;
  color: #333333;
  font-size: 0.9rem;
  background-color: #e8eaec;
  border-radius: 5px;
  padding: 0.05rem 0.6rem 0.2rem 0.6rem;
  margin-right: 0.3rem;
}

a.tag:hover {
  background-color: #5aabf4;
  box-shadow: inset 0 -3px 0 rgba(44, 49, 63, 0.15);
}
</style>

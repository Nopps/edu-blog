<template>
  <header class="main-header">
    <img class="main-header__img" :src="image" :alt="alt" />
  </header>
</template>

<script>
export default {
  props: {
    alt: { type: String, default: null },
    image: { type: String, default: '' },
  },
}
</script>

<style>
.main-header__img {
  object-fit: cover;
  width: 100%;
  height: 10rem;
  margin-bottom: 2.5em;
}

@media screen and (min-width: 481px) {
  .main-header__img {
    height: 15rem;
  }
}

@media screen and (min-width: 1200px) {
  .main-header__img {
    height: 20rem;
  }
}
</style>

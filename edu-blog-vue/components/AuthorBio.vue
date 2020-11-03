<template>
  <aside>
    <div class="author-bio">
      <img class="author-bio__img" :src="image" :alt="alt" />

      <div class="author-bio__text">
        <h5>
          <a
            :href="href"
            :target="target"
            :rel="target === '_blank' ? 'noopener noreferrer' : null"
            >{{ authorName }}</a
          >
        </h5>
        <p>
          {{ text }}
        </p>
      </div>
    </div>
  </aside>
</template>

<script>
export default {
  props: {
    alt: { type: String, default: null },
    image: { type: String, default: '' },
    href: { type: String, default: '' },
    target: { type: String, default: '' },
    authorName: { type: String, default: '' },
    text: { type: String, default: '' },
  },
}
</script>

<style>
aside {
  border-top: 1px solid lightgray;
  border-bottom: 1px solid lightgray;
}

.author-bio {
  display: grid;
  padding-top: 2rem;
  grid-template-rows: 50% 50%;
}

@media screen and (min-width: 481px) {
  .author-bio {
    grid-template-columns: auto auto;
  }
}

@media screen and (min-width: 1200px) {
  .author-bio {
    grid-template-columns: 20% 80%;
  }
}

.author-author-bio p {
  margin: 0;
}

.author-bio__img {
  height: 7.5rem;
  border-radius: 50%;
  margin-right: 2rem;
}
</style>

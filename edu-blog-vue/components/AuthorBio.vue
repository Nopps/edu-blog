<template>
  <aside>
    <div class="bio">
      <img class="bio__img" :src="image" :alt="alt" />

      <div class="bio__text">
        <h5>
          <a
            :href="href"
            :target="target"
            :rel="target === '_blank' ? 'noopener noreferrer' : null"
            >{{ authorName }}</a
          >
        </h5>
        <p>
          Author bio – Ut enim ad minim veniam, quis nostrud exercitation
          ullamco laboris nisi ut aliquip ex ea commodo consequat.
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
  },
}
</script>

<style>
aside {
  border-top: 1px solid lightgray;
  border-bottom: 1px solid lightgray;
}

.bio {
  display: grid;
  padding-top: 2rem;
  grid-template-rows: 50% 50%;
}

@media screen and (min-width: 481px) {
  .bio {
    grid-template-columns: auto auto;
  }
}

@media screen and (min-width: 1200px) {
  .bio {
    grid-template-columns: 20% 80%;
  }
}

.bio p {
  margin: 0;
}

.bio__img {
  height: 7.5rem;
  border-radius: 50%;
  margin-right: 2rem;
}
</style>

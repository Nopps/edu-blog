<template>
  <div>
    <pre
      >{{ JSON.stringify(post, null, 2) }}
  </pre
    >
    <div v-if="post" class="container">
      <Header :image="post.header.image" :alt="post.header.alt" />
      <article>
        <time pubdate :datetime="date" :title="date">{{ post.date }}</time>
        <h1>{{ post.title }}</h1>
        <p class="lead">
          {{ lead }}
        </p>
        <template v-for="item in post.content">
          <p v-if="item.type === 'paragraph'" :key="item.id">
            {{ item.text }}
          </p>
          <ul v-if="item.type === 'ul'" :key="item.id">
            <li v-for="li in item.li" :key="li">{{ li }}</li>
          </ul>
          <ol v-if="item.type === 'ol'" :key="item.id">
            <li v-for="li in item.li" :key="li">{{ li }}</li>
          </ol>
          <h2 v-if="item.type === 'heading2'" :key="item.id">
            {{ item.text }}
          </h2>
          <h3 v-if="item.type === 'heading3'" :key="item.id">
            {{ item.text }}
          </h3>
          <h4 v-if="item.type === 'heading4'" :key="item.id">
            {{ item.text }}
          </h4>
          <div
            v-else-if="item.type === 'cols'"
            :key="item.id"
            class="article-col-container"
          >
            <div
              v-for="col in item.col"
              :key="col"
              class="article-col-container__col"
            >
              <ul v-if="col.type === 'ul'">
                <li v-for="li in col.li" :key="li">{{ li }}</li>
              </ul>
              <ol v-if="col.type === 'ol'">
                <li v-for="li in col.li" :key="li">{{ li }}</li>
              </ol>
            </div>
          </div>
        </template>
        <Tag
          v-for="tag in post.tags"
          :key="tag.id"
          :text="tag.text"
          :href="tag.url"
        />
      </article>
      <AuthorBio
        :image="post.author.image"
        :alt="post.author.alt"
        :url="post.author.url"
        :target="post.author.target"
        :name="post.author.name"
        :text="post.author.text"
      />
      <Footer text="Copyright 2020 Noppe" />
    </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Tag from '~/components/Tag.vue'
import AuthorBio from '~/components/AuthorBio.vue'
import Footer from '~/components/Footer.vue'
import '~/components/_global.css'
import BlogPost1 from '~/data/blogpost-1.json'
import BlogPost2 from '~/data/blogpost-2.json'

export default {
  components: {
    Header,
    Tag,
    AuthorBio,
    Footer,
  },
  fetch({ params, redirect }) {
    console.log('test', params.slug)
    if (params.slug === 'post1') {
      console.log('test', BlogPost1)
      this.post = BlogPost1
    } else if (params.slug === 'post2') {
      this.post = BlogPost2
    } else {
      redirect(307, '/error')
    }
  },
  fetchOnServer: false,
  data() {
    return {
      post: null,
    }
  },
  computed: {
    footer() {
      return 'Copyright ' + new Date().getFullYear() + ' Noppe'
    },
  },
}
</script>

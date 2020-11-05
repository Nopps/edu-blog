<template>
  <div class="container">
    <Header
      image="https://images.unsplash.com/photo-1546074177-ffdda98d214f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1567&q=80"
      alt="Header image with letter tiles that says Read More"
    />
    <article>
      <time pubdate :datetime="date" :title="date">{{ date }}</time>
      <h1>{{ title }}</h1>
      <p class="lead">
        {{ lead }}
      </p>
      <div v-for="item in content" :key="item.id">
        <p v-if="item.type === 'paragraph'">
          {{ item.text }}
        </p>
        <ul v-if="item.type === 'ul'">
          <li v-for="li in item.li" :key="li">{{ li }}</li>
        </ul>
        <ol v-if="item.type === 'ol'">
          <li v-for="li in item.li" :key="li">{{ li }}</li>
        </ol>
        <h2 v-if="item.type === 'heading2'">
          {{ item.text }}
        </h2>
        <h3 v-if="item.type === 'heading3'">
          {{ item.text }}
        </h3>
        <h4 v-if="item.type === 'heading4'">
          {{ item.text }}
        </h4>
        <div v-else-if="item.type === 'cols'" class="article-col-container">
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
      </div>
      <Tag v-for="tag in tags" :key="tag.id" :text="tag.text" :href="tag.url" />
    </article>
    <AuthorBio
      :image="author.image"
      :alt="author.alt"
      :url="author.url"
      :target="author.target"
      :name="author.name"
      :text="author.text"
    />
    <Footer text="Copyright 2020 Noppe" />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Tag from '~/components/Tag.vue'
import AuthorBio from '~/components/AuthorBio.vue'
import Footer from '~/components/Footer.vue'
import '~/components/_global.css'

export default {
  components: {
    Header,
    Tag,
    AuthorBio,
    Footer,
  },
  data() {
    return {
      title: 'Blog Post Title h1',
      date: '28. August 2020',
      lead:
        'Lead Paragraph – Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
      author: {
        image: 'https://avatars2.githubusercontent.com/u/1894309?s=120&v=4',
        alt: 'Author portrait',
        url: 'https://github.com/Nopps',
        target: '_blank',
        name: 'Noora S.',
        text:
          'Author bio – Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      },
      content: [
        {
          id: '1',
          type: 'heading2',
          text: 'Subtitle h2',
        },
        {
          id: '2',
          type: 'paragraph',
          text:
            'Paragraph – Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        {
          id: '3',
          type: 'heading3',
          text: 'Subtitle h3',
        },
        {
          id: '4',
          type: 'cols',
          col: [
            {
              type: 'ul',
              li: [
                'Lorem ipsum dolor sit amet',
                'Consectetur adipiscing elit',
                'Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua',
              ],
            },
            {
              type: 'ol',
              li: [
                'Duis aute irure dolor in reprehenderit in voluptate',
                'Quis nostrud exercitation ullamco laboris',
                'Excepteur sint occaecat cupidatat non proident',
              ],
            },
          ],
        },
        {
          id: '5',
          type: 'heading4',
          text: 'Subtitle h4',
        },
        {
          id: '6',
          type: 'ul',
          li: [
            'Lorem ipsum dolor sit amet',
            'Consectetur adipiscing elit',
            'Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua',
          ],
        },
        {
          id: '7',
          type: 'paragraph',
          text:
            'Paragraph – Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
      ],
      tags: [
        {
          id: '1',
          text: 'Tag 1',
          url: '/tag1.html',
        },
        {
          id: '2',
          text: 'Tag 2',
          url: '/tag2.html',
        },
        {
          id: '3',
          text: 'Tag 3',
          url: '/tag3.html',
        },
      ],
    }
  },
}
</script>

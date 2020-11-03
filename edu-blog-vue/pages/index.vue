<template>
  <div class="container">
    <Header
      image="https://images.unsplash.com/photo-1546074177-ffdda98d214f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1567&q=80"
      alt="Header image with letter tiles that says Read More"
    />
    <article>
      <time pubdate datetime="2020-08-28" title="August 28th, 2020"
        >28. August 2020</time
      >
      <h1>Blog Post Title h1</h1>
      <p class="lead">
        Lead Paragraph – Lorem ipsum dolor sit amet, consectetur adipiscing
        elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
        ut aliquip ex ea commodo consequat.
      </p>
      <h2>Subtitle h2</h2>
      <p>
        Paragraph – Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
        do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
        ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
        aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit
        in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
        Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
        officia deserunt mollit anim id est laborum.
      </p>
      <h3>Subtitle h3</h3>
      <div class="article-col-container">
        <div class="article-col-container__col">
          <ul>
            <li>Lorem ipsum dolor sit amet</li>
            <li>Consectetur adipiscing elit</li>
            <li>
              Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
            </li>
          </ul>
        </div>
        <div class="article-col-container__col">
          <ol>
            <li>Duis aute irure dolor in reprehenderit in voluptate</li>
            <li>Quis nostrud exercitation ullamco laboris</li>
            <li>Excepteur sint occaecat cupidatat non proident</li>
          </ol>
        </div>
      </div>
      <h4>Subtitle h4</h4>
      <ul>
        <li>Lorem ipsum dolor sit amet</li>
        <li>Consectetur adipiscing elit</li>
        <li>
          Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
        </li>
      </ul>
      <p>
        Paragraph – Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
        do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
        ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
        aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit
        in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
        Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
        officia <a href="">deserunt mollit</a> anim id est laborum.
      </p>
      <Tag text="Tag 1" href="#" />
      <Tag text="Tag 2" href="#" />
      <Tag text="Tag 3" href="#" />
    </article>
    <AuthorBio
      image="https://avatars2.githubusercontent.com/u/1894309?s=120&v=4"
      alt="Author portrait"
      href="https://github.com/Nopps"
      target="_blank"
      name="Noora S."
      text="Author bio – Ut enim ad minim veniam, quis nostrud exercitation
      ullamco laboris nisi ut aliquip ex ea commodo consequat."
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
}
</script>

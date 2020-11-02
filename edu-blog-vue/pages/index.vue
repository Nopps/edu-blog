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
      <Metatag text="Tag 1" href="#" />
      <Metatag text="Tag 2" href="#" />
      <Metatag text="Tag 3" href="#" />
    </article>
    <AuthorBio
      image="https://avatars2.githubusercontent.com/u/1894309?s=120&v=4"
      alt="Author portrait"
      href="https://github.com/Nopps"
      target="_blank"
      authorName="Noora S."
    />
    <Footer text="Copyright 2020 Noppe" />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Metatag from '~/components/Metatag.vue'
import AuthorBio from '~/components/AuthorBio.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: {
    Header,
    Metatag,
    AuthorBio,
    Footer,
  },
}
</script>

<style>
:root {
  --typo-scale: 1.2;
  font-size: 15px;
  font-family: 'Roboto', Arial, sans-serif;
  line-height: 1.5;
}

body {
  margin: 0;
}

@media screen and (min-width: 481px) {
  :root {
    font-size: 16px;
    --typo-scale: 1.25;
  }
}

@media screen and (min-width: 1200px) {
  :root {
    font-size: 17px;
    --typo-scale: 1.333;
  }
}

p {
  font-size: 1rem;
  margin-top: 0;
  margin-bottom: 1.5em;
}

.lead {
  font-size: calc(var(--typo-scale) * 1rem);
}

ul,
ol {
  padding-left: 1.5rem;
  margin-bottom: 1rem;
}

@media screen and (min-width: 481px) {
  ul,
  ol {
    padding-left: 2rem;
  }
}

@media screen and (min-width: 1200px) {
  ul,
  ol {
    padding-left: 2.4rem;
  }
}

a {
  display: inline-block;
  color: #026bcb;
  text-decoration: none;
  -webkit-transition: color 130ms ease-in, -webkit-box-shadow 130ms ease-in-out;
  transition: color 130ms ease-in, -webkit-box-shadow 130ms ease-in-out;
  transition: color 130ms ease-in, box-shadow 130ms ease-in-out;
  -webkit-box-shadow: inset 0 -2px 0 rgba(44, 49, 63, 0.3);
  box-shadow: inset 0 -2px 0 rgba(44, 49, 63, 0.3);
}

a:hover {
  color: #0255a2;
  -webkit-box-shadow: inset 0 -9px 0 rgba(44, 49, 63, 0.15);
  box-shadow: inset 0 -9px 0 rgba(44, 49, 63, 0.15);
}

h1,
h2,
h3,
h4,
h5 {
  font-family: 'Poppins', Arial, sans-serif;
  font-weight: 700;
  line-height: 1.2;
  margin-top: 1.2em;
  margin-bottom: 0.3em;
}

h1 {
  font-size: calc(
    var(--typo-scale) * var(--typo-scale) * var(--typo-scale) *
      var(--typo-scale) * var(--typo-scale) * 1rem
  );
  margin-top: 0;
  margin-bottom: 0.5em;
}

h2 {
  font-size: calc(
    var(--typo-scale) * var(--typo-scale) * var(--typo-scale) *
      var(--typo-scale) * 1rem
  );
}

h3 {
  font-size: calc(
    var(--typo-scale) * var(--typo-scale) * var(--typo-scale) * 1rem
  );
}

h4 {
  font-size: calc(var(--typo-scale) * var(--typo-scale) * 1rem);
}
h5 {
  font-size: calc(var(--typo-scale) * 1rem);
}

@media screen and (min-width: 481px) {
  .bio h5 {
    margin-top: 0;
  }
}

time {
  border-bottom: 1px solid #dfdfdf;
  display: block;
  margin-bottom: 2rem;
  padding-bottom: 0.2rem;
  font-size: 0.9rem;
  font-family: 'Poppins', Arial, sans-serif;
  color: #646464;
}

/* LAYOUT */

.article-col-container {
  display: grid;
  grid-template-rows: auto auto;
}

.article-col-container__col ol,
.article-col-container__col ul {
  margin-top: 0;
}

@media screen and (min-width: 481px) {
  .article-col-container {
    grid-template-rows: auto auto;
  }
  .article-col-container__col ol,
  .article-col-container__col ul {
    margin-top: 0;
  }
}

@media screen and (min-width: 1200px) {
  .article-col-container {
    grid-template-columns: 50% 50%;
  }

  .article-col-container__col ol,
  .article-col-container__col ul {
    margin-top: 0;
  }
}

article,
.bio,
footer {
  width: 90%;
  margin: 0 auto 2rem auto;
}

@media screen and (min-width: 481px) {
  article,
  .bio,
  footer {
    width: 70%;
  }
}

@media screen and (min-width: 1200px) {
  article,
  .bio,
  footer {
    max-width: 60rem;
  }
}
</style>

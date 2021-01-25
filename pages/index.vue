<template>
  <div>
    <Container>
      <Hero class="background" />
      <h1>Digital presence for your business</h1>
    </Container>
    <section>
      <Container class="button">
        <nuxt-link to="/services"> <button>Services</button></nuxt-link>
        <nuxt-link to="/contact"> <button>Contact</button></nuxt-link>
        <nuxt-link to="/coding"> <button>Coding</button></nuxt-link>
      </Container>
      <Container flex class="blog">
        <ArticleCard
          v-for="(blog, index) in blogList"
          :key="index"
          :index="index"
          :article-info="blog"
        />
        <nuxt-link to="/blog"
          ><p class="posts">See all of ours posts</p></nuxt-link
        >
      </Container>
    </section>
  </div>
</template>

<script>
import ArticleCard from '~/components/ArticleCard'
import Container from '~/components/Container'

import blogs from '~/content/blogs.json'

export default {
  components: {
    ArticleCard,
    Container,
  },

  async asyncData({ app }) {
    async function awaitImport(blog) {
      const wholeMD = await import(`~/content/blog/${blog.slug}.md`)
      return {
        attributes: wholeMD.attributes,
        link: blog.slug,
      }
    }

    const blogList = await Promise.all(
      blogs.slice(0, 2).map((blog) => awaitImport(blog))
    ).then((res) => {
      return {
        blogList: res,
      }
    })

    return blogList
  },
}
</script>

<style scoped>
.background {
  background-color: #edbd54;
  margin-top: 5%;
}
body {
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100vh;
  overflow: hid;
}

.button {
  display: flex;
  justify-content: space-around;
  margin-bottom: 20px;
  margin-top: 20px;
}

h1 {
  margin-top: 0;
  line-height: 2.1;
  color: #28430a;
}

button {
  border: 0;
  background: transparent;
  border-radius: 0;
  font-weight: inherit;
  letter-spacing: inherit;
  line-height: inherit;
  text-transform: inherit;
  background-color: #793000;
  color: #fff;

  position: relative;
  z-index: 0;
  display: inline-block;
  overflow: hidden;
  font-size: 1rem;
  /* padding: 14.00778px 20px; */
  /* padding: 14.00778px -1px; */
  border-radius: 2em;
  cursor: pointer;
}
.posts {
  font-weight: bold;
  text-decoration: underline;
}
.blog {
  display: flex;
  flex-direction: column;
}

@media (min-width: 720px) {
  button {
    border: 0;
    background: transparent;
    border-radius: 0;
    font-weight: inherit;
    letter-spacing: inherit;
    line-height: inherit;
    text-transform: inherit;
    background-color: #793000;
    color: #fff;
    position: relative;
    z-index: 0;
    display: inline-block;
    overflow: hidden;
    font-size: 1.125rem;
    padding: 14.00778px 20px;
    border-radius: 2em;
    cursor: pointer;
  }
}

@media (max-width: 992px) {
  h1 {
    font-size: larger;
  }
}
</style>

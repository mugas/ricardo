<template>
  <section>
    <Container>
      <div class="intro">
        <h1>Let's code</h1>
      </div>
    </Container>
    <Container flex>
      <Coding
        v-for="(coding, index) in codingList"
        :key="index"
        :index="index"
        :article-info="coding"
      />
    </Container>
  </section>
</template>

<script>
import codings from '~/content/codings.json'

export default {
  async asyncData({ app }) {
    async function awaitImport(coding) {
      const wholeMD = await import(`~/content/coding/${coding.slug}.md`)
      return {
        attributes: wholeMD.attributes,
        link: coding.slug,
      }
    }

    const codingList = await Promise.all(
      codings.map((blog) => awaitImport(blog))
    ).then((res) => {
      return {
        codingList: res,
      }
    })
    return codingList
  },
}
</script>

<style scoped>
h1 {
  color: #28430a;
  margin-bottom: 2rem;
  margin-top: 2rem;
}
</style>

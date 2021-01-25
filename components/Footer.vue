<template>
  <footer class="footer">
    <section class="name">
      &copy; Good Stuff Creations {{ new Date().getFullYear() }}
    </section>
    <SocialMedia />
  </footer>
</template>

<style lang="scss">
.footer {
  display: flex;
  height: 100%;
  width: 100%;
  justify-content: space-between;

  padding: 2rem 0;
  color: black;
  @media (max-width: 567px) {
    padding: 1.2rem 0;
  }
  > * {
    margin-left: 2%;
    margin-right: 2%;
  }
}
</style>

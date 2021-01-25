<template>
  <div>
    <div class="page-wrapper">
      <aside>
        <h1>Hi, I'm Ricardo</h1>
        <p class="bio">
          Let's <br />
          <span class="action"> {{ actions[0] }}</span>
        </p>
        <p class="name">Ricardo Moreira</p>
        <p>firstname.lastname@gscreations.io</p>
        <SocialMedia />
      </aside>
      <article>
        <div class="image">
          <img src="~/assets/images/me.png" />
        </div>
        <div class="text">
          <p>
            My name is Ricardo Moreira and I am a Web developer. I was born in
            Portugal but I live in Finland with my wife and 2 daughters. Good
            Stuff Creations was created for 2 main reasons: A web more
            accessible and sustainable for all focused on the
            <nuxt-link to="/services">Hospitality</nuxt-link>
            business, and <nuxt-link to="/coding">tutorials</nuxt-link>,
            courses, and e-books for parents and/or people with a day-job that
            want to learn to code.
          </p>
          <p>
            Before I learn web development, I spent many years working for
            hospitality. From bars, hotel to restaurants, from waiter to kitchen
            helper, manager, or owner I did a bit of all. Every day more the
            world is getting more digital and many companies are still lacking
            in this aspect, only having their digital presence in a Social Media
            that they can't control or have an old website that doesn't deliver
            the results it should. I want to help close that gap. With your
            help, and my knowledge from both sides ( web development and
            hospitality) I can deliver you a
            <nuxt-link to="/services">solution</nuxt-link> that helps you
            business grows, either by creating a new website or finding the best
            digital strategy for your company. Lately, I have been focusing in
            accessibility and sustainability(yes your website can and it should
            be more sustainable) and the more I know the more I find it
            important to create digital solutions that are better for all and
            that reduce your carbon footprint.
          </p>
          <p>
            I'm not a developer by trade. I learn on my "own"(thank you internet
            and all great programming courses out there) while having a shift
            job and being a parent and it's not an easy road but it's a
            possible, challenging, and worth take it on. So I know that are many
            people like me, parents or not that have a day job and are new to
            coding but want to learn to code because they want to get into this
            career, because they have a great business idea and learning to code
            helps them achieve that or just because. Without a network, and with
            few free time can be daunting, so I want that my
            <nuxt-link to="/coding">tutorials</nuxt-link> and courses can help a
            bit your road to reach your goal. Also, feel free to connect with me
            <nuxt-link to="/contact">here</nuxt-link> or with the
            <a href="https://twitter.com/mugas11">bluebird</a>
            help for any question that may arise you.
          </p>
          <p>
            You can learn more about me in my personal
            <a href="http://ricardomoreira.io/">website</a> and follow my and
            Good Stuff Creations social media.
          </p>
        </div>
      </article>
    </div>
    <footer></footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      actions: ['Talk', 'Work', 'Connect'],
    }
  },
  mounted() {
    window.setInterval(() => {
      this.pollPerson()
    }, 5000)
  },
  methods: {
    pollPerson() {
      const first = this.actions.shift()
      this.actions = this.actions.concat(first)
    },
  },
}
</script>

<style scoped>
body {
  margin: 0;
  font-family: 'Cormorant Garamond', serif;
  font-size: 18px;
}
a {
  box-shadow: inset 0 -1px 0 currentColor;
}
a:hover {
  box-shadow: inset 0 0 0 currentcolor, 0 3px 0 currentcolor;
}
.name {
  margin-bottom: 0;
}
.action {
  color: #793000;
  font-size: 11.5vw;
  filter: brightness(2);
}

.page-wrapper {
  display: block;
  width: 100%;
}

@media (min-width: 700px) {
  .page-wrapper {
    display: flex;
  }

  .action {
    color: #793000;
    font-size: 3.5vw;
    filter: brightness(2);
  }
}
aside {
  background-color: #28430a;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px 0 40px;
}

@media (min-width: 700px) {
  aside {
    background-color: #28430a;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    width: 50%;
    flex: 0 0 50%;
    padding: 0;
  }
}
h1,
.flourish {
  font-size: 6vw;
  margin: 10px 0;
  font-family: 'Oxygen', sans-serif;
  text-align: center;
}

@media (min-width: 700px) {
  h1,
  .flourish {
    font-size: 4.5vw;
    margin: 20px 0;
    padding: 0 20px;
  }
}
h1 {
  letter-spacing: 10px;
  text-transform: uppercase;
}

.flourish {
  font-weight: bold;
}

.bio {
  margin: 0 20px;
  text-align: center;
  line-height: 1.5;
  font-style: italic;
}

@media (min-width: 1100px) {
  .bio {
    text-align: center;
    line-height: 1.7;
    margin-bottom: 1.6em;
    font-size: 1.2em;
  }
}
article {
  margin: 0;
}

@media (min-width: 700px) {
  article {
    flex: 0 0 50%;
    margin-left: 50%;
    padding-top: 30px;
  }
}
.author,
.photographer {
  text-transform: uppercase;
  font-size: 0.7em;
  letter-spacing: 1px;
  color: #777;
  padding: 0 20px;
  margin: 0;
  font-family: 'Oxygen', sans-serif;
}
.author span,
.photographer span {
  color: rgba(0, 0, 0, 0.4);
  text-transform: capitalize;
}

@media (min-width: 700px) {
  .author,
  .photographer {
    padding: 0 60px;
  }
}
.image img {
  width: 100%;
  height: 50%;
  margin: 20px 0;
}

.text {
  columns: 2;
  column-width: 250px;
  column-gap: 2em;
  padding: 0 20px;
  text-align: justify;
}
.text p:first-child {
  margin-top: 0;
}
.text p:first-child:first-letter {
  float: left;
  color: #793000;
  font-size: 4em;
  line-height: 35px;
  padding: 19px 10px 10px 0;
}

@media (min-width: 1100px) {
}
footer {
  height: 40px;
}
</style>

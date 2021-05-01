<template lang="html" class="homepage">
  <div>
    <header class="header">
      <h1 class="title">
        I create <span class="action">{{ actions[0] }} </span>and stuff
      </h1>
      <p class="subtitle">Developer, entrepreneur and constant learner</p>
      <button>Let's Work together</button>
    </header>
    <section class="stuff">
      <h2>Some of my projects</h2>
      <article class="websites card">
        <h3>Good Stuff Creations</h3>
        <p class="websites__paragraph">
          Website and digital products for local producers and groceries
        </p>
        <button>To the Website</button>
        <p class="card__footer">Web development, Wordpress, SEO</p>
      </article>
      <article class="podcasts card">
        <h3>Podcast</h3>
        <p class="websites__paragraph">Coming Soon</p>
      </article>
      <article class="food card">
        <h3>Good Stuff Foods</h3>
        <p class="websites__paragraph">Coming Soon</p>
      </article>
    </section>
  </div>
</template>

<script>
export default {
  layout: 'empty',
  data() {
    return {
      actions: [
        'Things',
        'Podcasts',
        'Websites',
        'Food',
        'Writing',
        'Code',
        'Courses',
      ],
    }
  },
  mounted() {
    window.setInterval(() => {
      this.pollPerson()
    }, 3000)
  },
  methods: {
    pollPerson() {
      const first = this.actions.shift()
      this.actions = this.actions.concat(first)
    },
  },
}
</script>

<style lang="css" scoped>
/*General*/

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  padding-top: 10px;
}

html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
}
/*Header*/

.header {
  display: flex;
  flex-direction: column;
  /* background-color: black; */
  margin-left: 2%;
  margin-right: 2%;
  height: 67vh;
  background-color: #000000;
  background-image: linear-gradient(147deg, #000000 0%, #434343 74%);
}

.title {
  margin-left: 5%;
  font-size: 32px;
  overflow: hidden; /* content is not revealed until the animation */
  /*border-right: 0.09em solid #a64e43; The typwriter cursor */
  /* white-space: nowrap; Keeps the content on a single line */
  /* margin: 0 auto; Gives that scrolling effect as the typing happens */
  letter-spacing: 0.12em;
  animation: typing 6.5s steps(40, end), blinking 0.5s step-end infinite;
  width: 93%;
  line-height: 50px;
  padding-bottom: 32px;
  color: white;
}

.subtitle {
  margin-left: 5%;
  padding-bottom: 8%;
  font-size: 18px;
  line-height: 26px;
  color: white;
  padding-bottom: 52px;
}
.action {
  color: yellow;
}

button {
  border: 0;
  background: transparent;
  border-radius: 0;
  margin-top: 3%;
  margin-left: 5%;
  font-weight: inherit;
  letter-spacing: inherit;
  line-height: inherit;
  text-transform: inherit;
  background-color: white;
  color: #000;
  position: relative;
  z-index: 0;
  display: inline-block;
  overflow: hidden;
  font-size: 1rem;
  padding: 14.00778px 20px;
  border-radius: 2em;
  width: 59%;
  cursor: pointer;
  transition: all 0.5s;
}
button:hover {
  background-color: transparent;
  color: yellow;
  border: 2px solid yellow;
  font-size: 1rem;
  width: 20%;
}

button:active {
  background-color: transparent;
  color: yellow;
  border: 2px solid yellow;
  font-size: 1rem;
  width: 20%;
}
/*Other Projects*/
h2 {
  margin-left: 5%;
  text-align: center;
  font-size: 28px;
  line-height: 50px;
  padding-bottom: 32px;
}
h3 {
  font-size: 26px;
  margin-left: 5%;
  padding-bottom: 32px;
}
.stuff {
  display: flex;
  flex-direction: column;
}
.card {
  display: flex;
  flex-direction: column;
  margin-right: 6%;
  height: 60vh;
  border-radius: 10px;
  margin-bottom: 12%;
  margin-left: 6%;
}
.websites {
  color: white;
  background-color: #28430a;
}
.websites__paragraph {
  margin-left: 5%;
  padding-bottom: 32px;
}
.card__footer {
  position: relative;
  top: 113px;
  margin-left: 5%;
}
.podcasts {
  background-color: yellow;
}

.food {
  background-color: brown;
}

/*Animation*/

/* The typing effect */
@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 60%;
  }
}

/* The typewriter cursor effect */
@keyframes blinking {
  from,
  to {
    border-color: transparent;
  }
  50% {
    border-color: #a64e43;
  }
  100% {
    border-color: transparent;
  }
}

/*Media Queries*/

@media (min-width: 768px) {
  h1 {
    font-size: 45px;
  }
}
</style>

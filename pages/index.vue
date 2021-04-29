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
      <article class="websites"><h2>Good Stuff Creations</h2></article>
      <article class="podcasts"><h2>Good Stuff Creations</h2></article>
      <article class="food"><h2>Good Stuff Creations</h2></article>
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
.websites {
  color: white;
  background-color: green;
  margin-left: 2%;
  margin-right: 2%;
  height: 40vh;
  width: 100%;
}
.stuff {
  display: flex;
  flex-wrap: wrap;
  height: 100vh;
  justify-content: space-between;
}
.podcasts {
  background-color: yellow;
  margin-left: 2%;
  margin-right: 2%;
  height: 40vh;
  width: 40%;
}
.subtitle {
  margin-left: 5%;
  padding-bottom: 8%;
  font-size: 6vh;
  color: white;
}
.food {
  background-color: brown;
  margin-left: 2%;
  margin-right: 2%;
  height: 40vh;
  width: 40%;
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
  width: 15%;
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

.header {
  display: flex;
  flex-direction: column;
  /* background-color: black; */
  margin-left: 2%;
  margin-right: 2%;
  height: 80vh;
  background-color: #000000;
  background-image: linear-gradient(147deg, #000000 0%, #434343 74%);
}

h1 {
  font-size: 32px;
  color: white;
}

.bio {
  margin: 0 20px;
  text-align: center;
  line-height: 1.5;
  font-style: italic;
}
.title {
  margin-left: 5%;
  font-size: 10vh;
  overflow: hidden; /* content is not revealed until the animation */
  /*border-right: 0.09em solid #a64e43; The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  /* margin: 0 auto; Gives that scrolling effect as the typing happens */
  letter-spacing: 0.12em;
  animation: typing 6.5s steps(40, end), blinking 0.5s step-end infinite;
  width: 87%;
}

.main__letter-k {
  color: #a64e43;
}

.main__king-word {
  color: #a64e43;
}

.main__question-mark {
  color: #a64e43;
  -webkit-animation: bounce-in-top 1s 11s both;
  animation: bounce-in-top 1s 11s both;
  display: inline-block;
}

.main__bounce-first {
  -webkit-animation: bounce-in-top 7.1s both;
  animation: bounce-in-top 7.1s both;
  display: inline-block;
  color: #a64e43;
}

.main__bounce-second {
  -webkit-animation: bounce-in-top 10.1s both;
  animation: bounce-in-top 10.1s both;
  display: inline-block;
  color: #a64e43;
}

.main__bounce-third {
  -webkit-animation: bounce-in-top 1s 10s both;
  animation: bounce-in-top 1s 10s both;
  display: inline-block;
  color: #a64e43;
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

@-webkit-keyframes bounce-in-top {
  0% {
    -webkit-transform: translateY(-500px);
    transform: translateY(-500px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
    opacity: 0;
  }
  38% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
    opacity: 1;
  }
  55% {
    -webkit-transform: translateY(-65px);
    transform: translateY(-65px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  72% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  81% {
    -webkit-transform: translateY(-28px);
    transform: translateY(-28px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  90% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  95% {
    -webkit-transform: translateY(-8px);
    transform: translateY(-8px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
}

@keyframes bounce-in-top {
  0% {
    -webkit-transform: translateY(-500px);
    transform: translateY(-500px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
    opacity: 0;
  }
  38% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
    opacity: 1;
  }
  55% {
    -webkit-transform: translateY(-65px);
    transform: translateY(-65px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  72% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  81% {
    -webkit-transform: translateY(-28px);
    transform: translateY(-28px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  90% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
  95% {
    -webkit-transform: translateY(-8px);
    transform: translateY(-8px);
    -webkit-animation-timing-function: ease-in;
    animation-timing-function: ease-in;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    -webkit-animation-timing-function: ease-out;
    animation-timing-function: ease-out;
  }
}

/*Media Queries*/

@media (min-width: 768px) {
  h1 {
    font-size: 45px;
  }

  .main {
    flex-direction: column;
    justify-content: space-between;
  }
}
</style>

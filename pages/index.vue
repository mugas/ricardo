<template lang="html" class="homepage">
  <div class="main">
    <h1>
      <span class="main__bounce-second">L</span
      ><span class="main__bounce-third">oo</span
      ><span class="main__letter-k">k</span
      ><span class="main__king-word">ing</span>
      <span class="main__bounce-first">f</span>or Me<span
        class="main__question-mark"
        >?</span
      >
    </h1>
    <p>I create things and stuff</p>
  </div>
</template>

<style lang="css" scoped>
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
}

.main {
  background: url('../assets/me.jpg') no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  margin-left: 2%;
  margin-right: 2%;
  height: 85vh;
  margin-top: 6%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

h1 {
  text-align: center;
  font-size: 32px;
  color: #a64e43;
}

p {
  text-align: center;
  color: #eceee5;
  font-family: 'Inknut Antiqua', serif;
  overflow: hidden; /* content is not revealed until the animation */
  border-right: 0.09em solid #a64e43; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: 0.12em;
  animation: typing 6.5s steps(40, end), blinking 0.5s step-end infinite;
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
    width: 100%;
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
    text-align: center;
    font-size: 150px;
  }

  p {
    font-size: 10vh;
  }

  .main {
    flex-direction: column;
    justify-content: space-between;
  }
}
</style>

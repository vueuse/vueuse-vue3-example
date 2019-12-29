<template>
  <div id="app">
    <img src="./logo.svg" />
    <h1>Hello <a href='https://github.com/vuejs/vue-next' target='__blank'>Vue 3</a> and <a href='https://github.com/antfu/vueuse' target='__blank'>VueUse</a>!</h1>

    <h2>{{new Date(now)}}</h2>
  </div>
</template>

<script>
import { ref } from 'vue'
import { useNow } from '@vueuse/core'

export default {
  setup() {
    const now = useNow()

    return {
      now
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Noto+Serif&display=swap');

html, body, h1, h2, h3, p {
  font-family: 'Noto Serif', serif;
}

#app {
  text-align: center;
  color: rgba(0,0,0,0.4);
}
img {
  width: 500px;
}
a {
  color: #41b883;
  text-decoration: none;
}
</style>

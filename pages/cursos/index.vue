<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        Mis Cursos
      </h1>
      <ul v-for="item in cursos" :key="item">
        <li><nuxt-link :to="item.path">{{ item.name }}</nuxt-link></li>
      </ul>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  data() {
    return {
      cursos: [
          {name: 'Laravel 5.8', path: 'laravel'},
          {name: 'Introducción a la programación', path: 'programming'},
          {name: 'Vue.js 2', path: 'vue2'},
      ]
    }
  },
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

<template>
  <div class="layout">
    <Logo />
    <Nuxt />
    <Nav />
    <Footer />
  </div>
</template>

<script>
import Logo from '../components/Logo'
import Nav from '../components/Nav'
import Footer from '../components/Footer'

export default {
  name: 'App',
  components: {
    Logo,
    Nav,
    Footer,
  },
  // async asyncData({ params, $http }) {
  //   const content = await $http.$get(
  //     `https:${params.projectId}.apicdn.sanity.io/v1/data/query/${params.dataset}?=${params.query}`
  //   )
  //   return { content }
  // },
  // data() {
  //   return {
  //     params: {
  //       projectId: 'bh6rj5zs',
  //       dataset: 'production',
  //       token: '',
  //       useCdn: true,
  //       query: '*[_id == "2178d82d-cc98-4547-80d7-2bd480d6cf03"]',
  //     },
  //   }
  // },
}
</script>

<style>
html {
  font-family: 'Roboto', sans-serif;
  font-size: 62.5%;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  position: relative;
  background-color: #fcf9ee;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>

<template>
  <section class="gallery">
    <Carousel
      class="gallery__carousel"
      :per-page-custom="[
        [0, 1],
        [750, 2],
        [1200, 3],
        [1600, 4],
        [2200, 5],
      ]"
      :pagination-enabled="true"
      :autoplay="true"
      :loop="true"
      :speed="1000"
      :center-mode="true"
    >
      <Slide v-for="product of incomingData" :key="product._id">
        <Card :details="product" />
      </Slide>
    </Carousel>
  </section>
</template>

<script>
import sanityClient from '@sanity/client'
import Card from './ItemCard'

export default {
  name: 'HomeGallery',
  components: {
    Card,
  },
  data() {
    return {
      incomingData: [],
    }
  },
  async fetch() {
    const client = sanityClient({
      projectId: 'bh6rj5zs',
      dataset: 'production',
      token: '',
      useCdn: true,
    })
    const query = '*[_type == "product"]'
    const siteContent = await client
      .fetch(query)
      .then((content) => {
        return content
      })
      .catch((error) => {
        console.log(error)
      })
    this.incomingData = siteContent
    return siteContent
  },
}
</script>

<style scoped>
.gallery {
  margin: 5rem 0 20rem;
  padding: 0 1rem;
}
</style>

<template>
  <div class="container">
    <HomeHeader :content="content" />
    <HomeHighlights :content="content" />
    <HomeAbout :content="content" />
    <HomeCautionTape />
    <HomeGallery :content="content" />
  </div>
</template>

<script>
import HomeHeader from '../components/HomeHeader'
import HomeHighlights from '../components/HomeHighlights'
import HomeCautionTape from '../components/HomeCautionTape'
import HomeAbout from '../components/HomeAbout'
import HomeGallery from '../components/HomeGallery'

export default {
  components: {
    HomeHeader,
    HomeHighlights,
    HomeCautionTape,
    HomeAbout,
    HomeGallery,
  },
  async asyncData({ $http }) {
    const params = {
      projectId: 'bh6rj5zs',
      dataset: 'production',
      token: '',
      useCdn: true,
      query: '*[_id == "2178d82d-cc98-4547-80d7-2bd480d6cf03"]',
    }
    const incomingData = await $http.$get(
      `https://${params.projectId}.api.sanity.io/v1/data/query/${params.dataset}?query=${params.query}`
    )
    const content = incomingData.result[0]
    return { content }
  },
  data() {
    return {
      params: {
        projectId: 'bh6rj5zs',
        dataset: 'production',
        token: '',
        useCdn: true,
        query: '*[_id == "2178d82d-cc98-4547-80d7-2bd480d6cf03"]',
      },
    }
  },
}
</script>

<style>
.container {
  width: 100%;
  min-height: 100vh;
}
</style>

<template>
  <section class="card">
    <a :href="details.depopUrl" class="card__anchor-cover">
      <div class="card__image-container">
        <img class="card__image" :src="getURL()" alt="Shoe" />
      </div>
      <div class="card__details">
        <p class="card__collection">{{ details.description }}</p>
        <h2 class="card__title">{{ details.title }}</h2>
        <p class="card__price">{{ details.price }}</p>
      </div>
    </a>
  </section>
</template>

<script>
export default {
  name: 'ItemCard',
  props: ['details'],
  head() {
    return {
      link: [
        {
          rel: 'stylesheet',
          href:
            'https://fonts.googleapis.com/css2?family=Bahianita&family=Raleway&display=swap',
        },
      ],
    }
  },
  computed: {
    getURL() {
      return () => {
        const imageRef = this.details.image.image.asset._ref.split('-')
        return `https://cdn.sanity.io/images/bh6rj5zs/production/${imageRef[1]}-${imageRef[2]}.${imageRef[3]}`
      }
    },
  },
}
</script>

<style scoped>
.card {
  width: 100%;
  height: min-content;
  max-width: 350px;
  padding: 3rem 1rem;
  margin: 0 auto;
  background-color: #e7d6c4;
  border: 2px solid black;
}

.card__anchor-cover {
  text-decoration: none;
  color: inherit;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  gap: 1rem;
}

.card__image-container {
  overflow: hidden;
}

.card__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 50% 50%;
}

.card__details {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.card__collection {
  font-size: 1.6rem;
  font-weight: 400;
  line-height: 0.5;
}

.card__title {
  font-family: 'Bahianita', sans-serif;
  font-size: 7rem;
}

.card__price {
  font-family: 'Raleway', sans-serif;
  font-size: 3rem;
}

@media only screen and (min-width: 1700px) {
}
</style>

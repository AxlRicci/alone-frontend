<template>
  <section class="hh">
    <div class="hh__gallery">
      <div class="hh__image-container">
        <img class="hh__image hh__image--1" :src="getURL(0)" />
      </div>
      <div class="hh__image-container">
        <img class="hh__image hh__image--2" :src="getURL(1)" />
      </div>
    </div>
    <div class="hh__actions">
      <div class="hh__action-item">
        <NuxtLink to="/shop" class="hh__text-link">explore</NuxtLink>
        <NuxtLink to="/shop" class="hh__icon-link">
          <img
            class="hh__circle-icon"
            src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d14818767ac37ac193eccf4_circle-container.svg"
            alt=""
          />
          <img
            class="hh__arrow-icon"
            src="https://global-uploads.webflow.com/5c9c9c646cf0969b319f264f/5d24aa633c6cae18850994a2_arrow.svg"
            alt=""
          />
        </NuxtLink>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeHighlights',
  props: ['content'],
  computed: {
    getURL() {
      return (imageNumber) => {
        const imageRef = this.content.featuredImages[
          imageNumber
        ].asset._ref.split('-')
        return `https://cdn.sanity.io/images/bh6rj5zs/production/${imageRef[1]}-${imageRef[2]}.${imageRef[3]}`
      }
    },
  },
}
</script>

<style>
.hh {
  width: 100%;
  height: auto;
  margin-left: auto;
  padding: 0 5vw;
}

.hh__gallery {
  width: 100%;
  max-width: 1200px;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 1rem;
  margin-left: auto;
}

.hh__image-container {
  width: 100%;
  height: auto;
  border: 2px solid #000;
}

.hh__image {
  width: 100%;
  height: auto;
}

.hh__actions {
  padding: 3rem 0;
  display: flex;
  justify-content: flex-end;
}

.hh__action-item {
  width: auto;
  height: auto;

  display: flex;
  align-items: center;
  gap: 2rem;
}

.hh__text-link {
  font-size: 2rem;
  text-transform: uppercase;
  text-decoration: none;
  font-weight: 500;
  color: #000;
}

.hh__icon-link {
  width: auto;
  height: auto;
  position: relative;
}

.hh__circle-icon {
  width: 8rem;
  height: auto;
}

.hh__arrow-icon {
  width: 5rem;
  height: auto;

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

@media only screen and (min-width: 500px) {
  .hh__gallery {
    flex-direction: row;
    justify-content: flex-end;
  }
}

@media only screen and (min-width: 900px) {
  .hh {
    padding: 0 10vw 0 5vw;
  }
  .hh__gallery {
    gap: 3rem;
  }
}
</style>

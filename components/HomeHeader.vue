<template>
  <section class="header">
    <h2 class="header__title header__title-1">{{ content.headerLine_1 }}</h2>
    <span class="header__line">
      <h2 class="header__title header__title-2">{{ content.headerLine_2 }}</h2>
      <span class="header__collection">
        <p class="header__collection-text">{{ content.headerIndentLine_1 }}</p>
        <p class="header__collection-text">{{ content.headerIndentLine_2 }}</p>
      </span>
    </span>
  </section>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: ['content'],
}
</script>

<style scoped>
.header {
  width: 100%;
  height: auto;
  padding: 8rem 5vw 3rem 5vw;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.header__title {
  font-size: 17vw;
  font-weight: 500;
  margin: 0;
  line-height: 0.85;
  text-transform: uppercase;
}

.header__line {
  display: flex;
  align-items: flex-end;
  gap: 1rem;
}

.header__collection {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 0rem;
  font-family: 'Cyberthrone';
}

.header__collection-text {
  font-size: 7vw;
  text-transform: uppercase;
  font-style: italic;
  line-height: 0.65;
}

@media only screen and (min-width: 900px) {
  .header {
    padding: 10vh 10vw 3rem 10vw;
  }
}

@media only screen and (min-width: 1450px) {
  .header__title {
    font-size: 247px;
  }

  .header__collection-text {
    font-size: 100px;
  }
}
</style>

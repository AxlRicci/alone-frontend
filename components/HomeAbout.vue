<template>
  <section id="about" class="about">
    <div class="about__content">
      <div class="title">
        <h2>{{ content.aboutTitle }}</h2>
      </div>
      <p>
        {{ content.aboutContent }}
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeAbout',
  props: ['content'],
}
</script>

<style scoped>
.about {
  margin: 10rem 0;
  padding: 0 5vw;
  width: 100%;
  display: flex;
  justify-content: flex-end;
}

.about__content {
  font-size: 6vw;
  font-weight: 300;
  max-width: 1200px;
}

.title {
  float: left;
  font-size: 3vw;
  font-weight: 100;
  text-transform: uppercase;
  margin-right: 5rem;
}

@media only screen and (min-width: 600px) {
  .title {
    margin-right: 10rem;
  }
}
@media only screen and (min-width: 900px) {
  .about {
    padding: 0 10vw 0 5vw;
  }
}
@media only screen and (min-width: 1000px) {
  .about__content {
    font-size: 60px;
  }
  .title {
    font-size: 45px;
  }
}
@media only screen and (min-width: 1450px) {
  .about {
    padding: 0 10vw 0 5vw;
  }
}
</style>

<template>
  <nav class="nav">
    <ul class="nav__list">
      <li class="nav__item nav__item--shop">
        <a href="#shop" class="nav__link">shop</a>
      </li>
      <!-- <li class="nav__item">
        <NuxtLink to="/collections" class="nav__link">collections</NuxtLink>
      </li> -->
      <li class="nav__item">
        <a href="#about" class="nav__link">about</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
}
</script>

<style scoped>
.nav {
  position: absolute;
  top: 2rem;
  right: 5vw;
  height: 4rem;
  display: flex;
  align-items: center;
}

.nav__list {
  list-style-type: none;
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 0;
}

.nav__item {
  padding: 0.25rem 0;
  display: none;
}

.nav__item--shop {
  display: block;
}

.nav__link {
  text-decoration: none;
  color: #000;
  text-transform: uppercase;
  font-size: 1.6rem;
}

@media only screen and (min-width: 400px) {
  .nav__item {
    display: block;
  }
}

@media only screen and (min-width: 900px) {
  .nav {
    right: 10vw;
  }
}

@media only screen and (min-width: 1500px) {
  .nav {
    position: fixed;
    top: auto;
    bottom: 6rem;
    left: 5vw;
  }
  .nav__list {
    display: block;
    padding: 0;
  }
}

/* .nav {
  position: fixed;
  bottom: 5rem;
  left: 4vw;
}

.nav__list {
  list-style-type: none;
}

.nav__item {
  padding: 0.25rem 0;
}

.nav__link {
  text-decoration: none;
  color: #000;
  text-transform: uppercase;
  font-size: 1.6rem;
} */
</style>

<template>
  <NuxtLink to="/" class="logo">
    <h1 class="title">Alone</h1>
    <h1 class="title">Alone</h1>
  </NuxtLink>
</template>

<script>
export default {
  name: 'Logo',
}
</script>

<style scoped>
.logo {
  height: 4rem;
  width: auto;
  position: absolute;
  top: 2rem;
  left: 4vw;
  overflow: hidden;
  cursor: pointer;
  text-decoration: none;
  z-index: 1000;
}

.title {
  font-size: 3rem;
  color: #000;
  text-transform: uppercase;
  transition: all 0.4s;
}

.logo:hover .title {
  transform: translateY(-100%);
}

/* change to EMs */
@media only screen and (min-width: 1500px) {
  .logo {
    position: fixed;
    transform: rotate(270deg) translate(-50%, -50%);
  }
}
</style>

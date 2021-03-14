<template>
  <footer class="footer">
    <p class="copyright">Copyright <b>ALONE.</b> All Rights Reserved.</p>
    <div class="social-icons">
      <a class="social-icon-link" href="https://instagram.com">
        <img
          class="social-icon"
          src="@/assets/icons/instagram.svg"
          alt="Instagram Icon"
        />
      </a>
      <a class="social-icon-link" href="https://www.depop.com">
        <img
          class="social-icon"
          src="@/assets/icons/icons8-depop.svg"
          alt="Depop Icon"
        />
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped>
.footer {
  height: auto;
  width: 100%;
  padding: 1rem;
  position: absolute;
  bottom: 0;
  left: 0;
  display: flex;
  gap: 1rem;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

.copyright {
  font-size: 1.6rem;
  order: 1;
}

.social-icons {
  width: 30%;
  padding: 0 2rem;
  display: flex;
  justify-content: flex-end;
  gap: 2rem;
}

.social-icon-link {
  cursor: pointer;
}

.social-icon {
  height: 4rem;
  width: 4rem;
}

@media only screen and (min-width: 640px) {
  .footer {
    flex-direction: row;
  }
  .copyright {
    order: 0;
  }
}

@media only screen and (min-width: 900px) {
  .footer {
    padding: 0 10vw 0 5vw;
  }
}
</style>

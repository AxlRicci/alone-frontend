<template>
  <div id="shop" class="marquee" style="--tw: 151vw; --ad: 5s">
    <span>
      &nbsp;- ALONE SHOP - DO NOT SCROLL - ALONE SHOP - DO NOT SCROLL - ALONE
      SHOP - DO NOT SCROLL - ALONE SHOP - DO NOT SCROLL - ALONE SHOP - DO NOT
      SCROLL - ALONE SHOP - DO NOT SCROLL - ALONE SHOP - DO NOT SCROLL -</span
    >
  </div>
</template>

<script>
export default {
  name: 'TickerTape',
}
</script>

<style>
.marquee {
  margin: 10rem 0;
  font-size: 6vw;
  overflow: hidden;
  background-color: #ddc92a;
  border-top: 3px solid black;
  border-bottom: 3px solid black;
}

.marquee span {
  display: inline-block;
  white-space: nowrap;
  color: #00112c;
}

@media only screen and (min-width: 1000px) {
  .marquee {
    font-size: 60px;
  }
}
</style>

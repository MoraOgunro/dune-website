<template>
  <div class="footer">
      <p class="footer-text">Built with Vue.js 3 and custom Sass</p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="sass">
/* Wrap footer content in this */
.footer
    display: flex
    justify-content: center
    height: 2em
    background: rgba(0, 0, 0, 0.8)
.footer-text
    color: white
    font-size: 1em
    margin: auto
</style>

<template>
  <div class="full-screen">
    <div class="full-screen-content">
      <div class="top"></div>
      <div class="middle">
        <h1 class="text header">ARRAKIS</h1>
        <p class="text subtitle">A harsh desert planet located on the far edge of the Old Imperium in the Canopus star system.
Source of the Spice Melange, the most vital resource in the empire.</p>
      </div>
      <!-- Start of Foot Component !-->
      <div class="bottom">
        <CardContainer></CardContainer>
        <Footer></Footer>
      </div>
      <!-- End of Foot Component !-->
    </div>
  </div>
</template>

<script>
import CardContainer from './components/CardContainer.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    CardContainer,
    Footer
  }
}
</script>

<style lang='sass'>
$tablet: 600px
$medium-desktop: 768px
$desktop: 992px
$widescreen: 1200px
body, html
  margin: 0
  padding: 0
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  height: 100vh
/* Wrap page in this for full screen, must be used with full-screen-content class */
.full-screen
  display: flex
  width: 100vw
  height: 100%
  overflow-x: hidden
  overflow-y: hidden
  background-image: url("/src/assets/arrakis.png")
  background-position-x: center
  background-size: cover
/* Wrap all full screen content in this class */
.full-screen-content
  flex: 1
  display: flex
  flex-direction: column
  width: 100%
/* Wrap full screem header content */
.top
  flex-grow: 0
  flex-shrink: 1
  height: 3rem
  width: 100%
  min-height: 50px
/* Wrap full screen middle content */
.middle
  flex: 1
  min-height: 150px
  width: 100%
  .text
    color: white
    margin: auto
  .header
    font-size: 5rem
    margin-bottom: 2rem
    margin-top: 5vh
  .subtitle
    width: 90vw
    font-size: 1.1rem
/* Wrap footer content in this to get bottom allignment */
.bottom
  align-self: flex-end
  width: 100%
  flex-shrink: 1
  flex-grow: 0
@media screen and (max-width: $tablet)
  .full-screen
    overflow-y: auto
    scrollbar-color: black white
    scrollbar-width: thin
</style>

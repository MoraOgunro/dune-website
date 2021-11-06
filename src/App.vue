<template>
  <div class="full-screen">
    <div class="full-screen-content">
      <div class="top"></div>
      <div class="middle"></div>
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
    //  Card
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
/* Wrap all full screen content in this class */
.full-screen-content
  flex: 1
  display: flex
  flex-direction: column
  width: 100%
.top
  flex-grow: 0
  flex-shrink: 1
  flex-basis: 10vh
  height: 10vh
  width: 100%
  background-color: blue
.middle
  flex: 1
  width: 100%
  background-color: red
/* Wrap footer content in this to get bottom allignment */
.bottom
  align-self: flex-end
  width: 100%
  flex-shrink: 1
  flex-grow: 0
</style>

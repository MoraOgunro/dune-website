<template>
  <div class="full-screen">
      <CardContainer></CardContainer>
      <Footer></Footer>
  </div>
</template>

<script>
//  import Card from './components/Card.vue'
import CardContainer from './components/CardContainer.vue'
export default {
  name: 'App',
  components: {
    //  Card
    CardContainer
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
.full-screen
  width: 100vw
  height: 100%
  overflow-x: hidden
  overflow-y: hidden
  position: relative
</style>

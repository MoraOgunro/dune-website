<template>
  <div class="full-screen">
      <div class="card-container">
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
      </div>
  </div>
</template>

<script>
import Card from './components/Card.vue'
export default {
  name: 'App',
  components: {
    Card
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
.full-screen
  width: 100vw
  height: 100vh
  overflow-x: hidden
  overflow-y: hidden
.card-container
  display: grid
  grid-template-columns: repeat(3, 30vw)
  grid-template-rows: 30vw
  column-gap: 2vw
  padding: 0
  justify-content: space-evenly
  background-color: gray
@media screen and (min-width: $widescreen)
  .card-container
    width: auto
    justify-content: space-evenly
    padding: 0 10vw 0 10vw
    margin: auto
    grid-template-columns: repeat(3, max(30vh,300px))
    grid-template-rows: max(30vh,300px)
@media screen and (max-width: $tablet)
  .card-container
    row-gap: 2em
    grid-template-columns: 90vw
    grid-template-rows: repeat(3, 30vh)

</style>

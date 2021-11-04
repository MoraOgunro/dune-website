<template>
  <div class="card-container">
    <Card></Card>
    <Card></Card>
    <Card></Card>
  </div>
</template>

<script>
import Card from './Card.vue'
export default {
  components: {
    Card
  }
}
</script>

<style lang="sass">
$tablet: 600px
$medium-desktop: 768px
$desktop: 992px
$widescreen: 1200px
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

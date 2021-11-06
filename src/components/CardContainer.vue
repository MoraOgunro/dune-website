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
/* Wrap cards in this */
.card-container
  margin-bottom: 1rem
  display: grid
  grid-template-columns: repeat(3, 30vw)
  grid-template-rows: 30vw
  column-gap: 2vw
  width: 100%
  justify-content: space-evenly
  background-color: gray
@media screen and (min-width: $widescreen)
  .card-container
    grid-template-columns: repeat(3, max(30vh,250px))
    grid-template-rows: max(30vh,250px)
@media screen and (max-width: $tablet)
  .card-container
    grid-template-columns: 90vw
    grid-template-rows: repeat(3, 25%)
    height: 650px
    align-content: space-evenly
    justify-content: space-evenly
</style>

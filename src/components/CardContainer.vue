<template>
  <div class="card-container">
    <Card v-for="(url, index) in urls"
    :key="index"
    :imageURL="url">
    </Card>
  </div>
</template>

<script>
import Card from './Card.vue'
export default {
  components: {
    Card
  },
  data () {
    return {
      urls: ['PAUL.png', 'CHANI.png', 'LIET.png']
    }
  },
  methods: {
    send (message) {
      console.log(message)
    }
  }
}
</script>

<style lang="sass">
$tablet: 900px
$medium-desktop: 768px
$desktop: 992px
$widescreen: 1200px
/* Wrap cards in this */
.card-container
  margin-bottom: 1rem
  display: grid
  grid-template-columns: repeat(3, 30vw)
  grid-template-rows: 30vw
  column-gap: 0vw
  width: 100%
  justify-content: space-evenly
@media screen and (min-width: $widescreen)
  .card-container
    grid-template-columns: repeat(3, min(30vw,400px))
    grid-template-rows: min(30vw,400px)
@media screen and (max-width: $tablet)
  .card-container
    grid-template-columns: 90vw
    grid-template-rows: repeat(3, 25%)
    height: 650px
    align-content: space-evenly
    justify-content: space-evenly
</style>

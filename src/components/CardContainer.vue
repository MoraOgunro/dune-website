<template>
  <div class="card-container">
    <Card v-for="(person, index) in characters"
    :key="index"
    :imageURL="person.url"
    :name="person.name"
    :text="person.text">
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
      characters: [
        {
          name: 'Paul Atreites',
          text: 'Though he lacked companions his own age, he received tutelage from his teachers, men like Thufir Hawat, Duncan Idaho, Gurney Halleck',
          url: 'PAUL.png'
        },
        {
          name: 'Chani Kynes',
          text: 'Chani was born on Arrakis, the daughter of the half-Fremen planetologist Liet Kynes and his full-Fremen wife. She gradually developed into a formidable fighter, and by the time of her father\'s death was serving under naib Stilgar. ',
          url: 'CHANI.png'
        },
        {
          name: 'Liet Kynes',
          text: 'Liet Kynes inherited his father\'s mantle and served as both the planetary ecologist of Dune and leader of the Fremen. He continued his father\'s vision of gradually terraforming the planet from a harsh desert world into a temperate world with precipitation, greenery, and open water.',
          url: 'LIET.png'
        }
      ]
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

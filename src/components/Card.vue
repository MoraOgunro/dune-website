<template>
  <div class="card">
    <a href="#0"></a>
    <img class="card-image"
    :src="require(`../assets/${imageURL}`)" alt="">
    <div class="card-text-overlay">

      <div class="text-container">
        <div class="card-header">{{name}}</div>
        <div class="card-text">
          {{text}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['imageURL', 'name', 'text'],
  data () {
    return {
    }
  }

}
</script>

<style lang='sass'>
$tablet: 900px
$medium-desktop: 768px
$desktop: 992px
$widescreen: 1200px
$curve: 25px
/* Card styling */
.card
  box-shadow: 0px 0px 25px 12px rgba(0, 0, 0, 0.5)
  background-color: green
  border-radius: $curve
  overflow: hidden
  position: relative
  &:hover
    .card-text-overlay
      transform: translate3d(0, 0, 0)
    .text-container
      transform: translate3d(0, 2rem, 0)
.card-text-overlay
  border-radius: $curve
  display: flex
  flex-direction: column
  height: 100%
  position: absolute
  width: 100%
  top: 0
  transition: transform 300ms
  background-color: white
  transform: translate3d(0, calc(100% - 3rem), 0)
.card-image
  width: 100%
  height: 100%
  object-fit: cover
.text-container
  transition: transform 300ms
  transform: translate3d(0, 0, 0)
  height: 100%
  width: 90%
  margin: auto
  display: flex
  flex-direction: column
.card-header
  font-size: 1.75rem
  margin-top: 0.4rem
  margin-bottom: 1rem
.card-text
  color: black

@media screen and (max-width: $tablet)
  .card
    &:hover
      .card-text-overlay
        transform: translate3d(0, 0, 0)
      .text-container
        transform: translate3d(0, 0, 0)
  .card-image
    object-position: top
</style>

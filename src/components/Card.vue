<template>
  <div class="card">
    <img class="card-image"
    :src="require(`../assets/${imageURL}`)" alt="">
  </div>
</template>

<script>
export default {
  props: ['imageURL'],
  data () {
    return {
    }
  }

}
</script>

<style lang='sass'>
$tablet: 600px
$medium-desktop: 768px
$desktop: 992px
$widescreen: 1200px
$curve: 25px
/* Card styling */
.card
  background-color: green
  border-radius: $curve
  overflow: hidden
.card-image
  width: 100%
  height: 100%
  object-fit: cover
</style>

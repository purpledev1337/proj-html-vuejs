<template>
  <div>
    <hr>
      {{ productName }},
      {{ productPriceMin }} -
      {{ productPriceMax }}
    <hr>
  </div>
</template>

<script>
export default {
  name: 'ProductSlideCard',
  props: {
    productName: String,
    productPriceMin: String,
    productPriceMax: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

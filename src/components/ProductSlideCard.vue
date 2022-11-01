<template>
  <div>
      <!-- {{ productName }},
      {{ productPriceMin }} -
      {{ productPriceMax }}
      <img :src="productPath" alt=""> -->
  </div>
</template>

<script>
export default {
  name: 'ProductSlideCard',
  props: {
    productName: String,
    productPath: String,
    productPriceMin: String,
    productPriceMax: String,
    productActive: Boolean,
    productType: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

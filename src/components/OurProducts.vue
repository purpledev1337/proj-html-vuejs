<template>
  <div>
    <ProductSlideCard
    id="card"
    v-for="product, i in productsData" :key="i"
    :productName="product.name"
    :productPriceMin="product.priceMin"
    :productPriceMax="product.priceMax"
    />
  </div>
</template>

<script>
import ProductSlideCard from "./ProductSlideCard.vue"

export default {
  name: 'OurProducts',
  props: {
    productsData : Array
  },
  components: {
    ProductSlideCard
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
 #card {
   width: 20%;
   color: blue;
 }
</style>

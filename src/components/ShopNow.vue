<template>
  <div>
    ShopNow
    <ProductSlideCard
    id="card"
    v-for="product, j in productsData" :key="j"
    :productName="product.name"
    :productPriceMin="product.priceMin"
    :productPriceMax="product.priceMax"
    />
  </div>
</template>

<script>
import ProductSlideCard from "./ProductSlideCard.vue"

export default {
  name: 'ShopNow',
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
div {
   display: flex;
   flex-direction: column;
   justify-content: flex-start;
   color: red;
 }
</style>

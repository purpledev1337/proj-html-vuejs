<template>
  <div>
      <OurProducts
      :productsData="products"/>

      <SpecialMoments/>

      <ShopNow
      :productsData="products"/>

      <Presentation/>

      <Locations/>

      <Social/>

  </div>
</template>

<script>
import OurProducts from './OurProducts.vue'
import SpecialMoments from './SpecialMoments.vue'
import ShopNow from './ShopNow.vue'
import Presentation from './Presentation.vue'
import Locations from './Locations.vue'
import Social from './Social.vue'


export default {
  name: 'Main',
  components: {
    OurProducts,
    SpecialMoments,
    ShopNow,
    Presentation,
    Locations,
    Social
  },
  data() {
    return {
      products: [
        {
          name: "Choco Chip Cookies",
          path: "../assets/choco-chip-cookies.jpg",
          priceMin: '$19.00',
          priceMax: '$39.00'
        },
        {
          name: "Strawberry Jam Cookies",
          path: "../assets/strawberry-jam-cookies.jpg",
          priceMin: '$24.00',
          priceMax: '$62.00'
        },
        {
          name: "Strawberry Donut",
          path: "../assets/strawberry-donut.jpg",
          priceMin: '$24.00',
          priceMax: '$42.00'
        },
        {
          name: "Perfect Macarons",
          path: "../assets/perfect-macarons.jpg",
          priceMin: '$18.00',
          priceMax: '$52.00'
        },
        {
          name: "Small Cupcake",
          path: "../assets/small-cupcake.jpg",
          priceMin: '$14.00',
          priceMax: '$29.00'
        },
        {
          name: "Cherry Cake",
          path: "../assets/cherry-cake.jpg",
          priceMin: '$59.00',
          priceMax: '$119.00'
        },
        {
          name: "Home Bread",
          path: "../assets/home-bread.jpg",
          priceMin: '$12.00',
          priceMax: '$19.00'
        },
        {
          name: "Premium Bread",
          path: "../assets/premium-bread.jpg",
          priceMin: '$18.00',
          priceMax: '$37.00'
        }
      ]
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

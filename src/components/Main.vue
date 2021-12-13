<template>
  <ul>
    MAIN
    <li>
      <OurProducts
      :productsData="this.products"/>
      Our Products - component with son (ProductSlideCard)
    </li>
    <li>
      <SpecialMoments/>
      Special Moments (static)
    </li>
    <li>
      <ShopNow
      :productsData="this.products"/>
      Shop Now - component with son (ProductSlideCard)
    </li>
    <li>
      <Presentation/>
      Info component (static)
    </li>
    <li>
      <Locations/>
      Locations component (static)
    </li>
    <li>
      <Social/>
      Social component (static)
    </li>
  </ul>
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
          name: "Cookie",
          path: "../assets/product.png",
          priceMin: '$19.00',
          priceMax: '$39.00'
        },
        {
          name: "Cake",
          path: "../assets/product.png",
          priceMin: '$24.00',
          priceMax: '$62.00'
        }
      ]
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

<template>
  <section>
    <div id="text">
      <h6>Our Products</h6>
      <h1>All our delectable pastries are baked fresh in our Kitchen very morning, and are made with all-natural, all organic ingredients.</h1>
      <div class="btn dark">Start Shopping</div>
    </div>
    <div id="products">
      <div class="card">
        <img src="../assets/choco-chip-cookies.jpg" alt="">
        <div class="overlay">
          <div class="hidden_text">
            <h3>Choco Chip Cookies</h3>
            <p>Cookies, Pastries</p>
            <span>$19.00 - $39.00</span>
          </div>
        </div>
        <div class="arrow left">
          <font-awesome-icon class="icon" :icon="['fas', 'chevron-left']"/>
        </div>
      </div>
      <div class="card">
        <img src="../assets/strawberry-jam-cookies.jpg" alt="">
        <div class="overlay">
          <div class="hidden_text">
            <h3>Strawberry Jam Cookies</h3>
            <p>Cookies, Pastries</p>
            <span>$24.00 - $62.00</span>
          </div>
        </div>
        <div class="arrow right">
          <font-awesome-icon class="icon" :icon="['fas', 'chevron-right']"/>
        </div>
      </div>
    </div>
      <ProductSlideCard
      class="card"
      :class="product.active ? 'active' : '' "
      v-for="product, i in productsData" :key="i"
      :productName="product.name"
      :productPriceMin="product.priceMin"
      :productPriceMax="product.priceMax"
      />
  </section>
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
section {
  height: 100vh;
  padding: 150px 0;
  display: flex;
  justify-content: space-between;

  #text {
    width: 40%;
    padding: 30px 50px;

    h6 {
      color: #c1c1c7;
      text-transform: uppercase;
    }

    h1 {
      color: #5b2ca2;
      font-size: 2.4em;
      margin: 30px 0;
    }

    button {
      padding: 10px;
      margin-top: 20px;
    }
  }

  #products {
    width: 60%;
    display: flex;
    justify-content: space-between;

    .card {
      width: calc(50% - 10px);
      position: relative;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

      .overlay {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        background-color: rgba(0, 0, 0, 0.3);
        display: none;
        justify-content: center;
        align-items: center;

        .hidden_text {
          text-align: center;
          vertical-align: middle;
          color: #fff;

          h3 {
            font-size: 1.5em;
          }

          p {
            margin: 10px 0;
          }

          span {
            font-size: 1.6em;
            margin-top: 40px;
          }
        }
      }

      &:hover .overlay {
        display: flex;
      }
    }

    .arrow {
      padding: 30px 15px;
      color: #fff;
      background-color: #5b2ca254;
      position: absolute;
      top: 50%;
      transform: translate(0, -50%);

      &.left {
        left: 0;
      }

      &.right {
        right: 0;
      }

      // &.icon {
        
      // }
    }
  }
}
</style>

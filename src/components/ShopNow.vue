<template>
  <section>
    <div id="text">
      <h1>Find a freshly baked product perfect for you</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid minus, itaque tenetur. Sed ac nulla id orci tempor.</p>
      <div class="btn dark">Show All Products</div>
    </div>
    <div id="products">
      <div class="card">
        <img src="../assets/choco-chip-cookies.jpg" alt="">
        <div class="overlay">
          <div class="hidden_text">
            <span>Select Options / Quick View</span>
          </div>
        </div>
        <div class="info_text">
          <h1>Chock Chip Cookies</h1>
          <span>$19.00 - $39.00</span>
        </div>
      </div>
      <div class="card">
        <img src="../assets/strawberry-jam-cookies.jpg" alt="">
        <div class="overlay">
          <div class="hidden_text">
            <span>Select Options / Quick View</span>
          </div>
        </div>
        <div class="info_text">
          <h1>Strawberry Jamp Cookies</h1>
          <span>$19.00 - $39.00</span>
        </div>
      </div>
      <div class="card">
        <img src="../assets/strawberry-donut.jpg" alt="">
        <div class="overlay">
          <div class="hidden_text">
            <span>Select Options / Quick View</span>
          </div>
        </div>
        <div class="info_text">
          <h1>Strawberry Donut</h1>
          <span>$24.00 - $42.00</span>
        </div>
      </div>
      <div class="card">
        <img src="../assets/perfect-macarons.jpg" alt="">
        <div class="overlay">
          <div class="hidden_text">
            <span>Select Options / Quick View</span>
          </div>
        </div>
        <div class="info_text">
          <h1>Perfect Macarons</h1>
          <span>$18.00 - $52.00</span>
        </div>
      </div>
        <div class="arrow left">
          <font-awesome-icon class="icon" :icon="['fas', 'chevron-left']"/>
        </div>
        <div class="arrow right">
          <font-awesome-icon class="icon" :icon="['fas', 'chevron-right']"/>
        </div>
    </div>
      <ProductSlideCard
      class="card"
      :class="product.active ? 'active' : '' "
      v-for="product, i in productsData" :key="i"
      :productName="product.name"
      :productPriceMin="product.priceMin"
      :productPriceMax="product.priceMax"
      :productType="product.type"
      />
  </section>
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
section {
  height: 100vh;
  display: flex;
  justify-content: space-between;

  #text {
    width: 25%;
    padding: 15% 30px;
    text-align: center;
    margin-right: 30px;

    h1 {
      color: #5b2ca2;
      font-size: 1.9em;
      margin-top: 150px;
      margin-bottom: 25px;
    }

    p {
      font-size: 1.2em;
      line-height: 25px;
      color: #818085;
    }
  }

  #products {
    width: 75%;
    padding: 16% 0;
    display: flex;
    justify-content: space-between;
    position: relative;

    .card {
      width: calc(25% - 15px);
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
        background-color: rgba(0, 0, 0, 0.4);
        display: none;
        justify-content: center;
        align-items: center;

        .hidden_text {
          text-align: center;
          vertical-align: middle;
          color: #d3d3d3;

          span {
            font-size: 1em;
            text-transform: uppercase;
          }
        }
      }

      &:hover .overlay {
        display: flex;
      }

      .info_text {
        padding: 20px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        color: #5b2ca2;

        h1 {
          font-size: 1.2em;
        }

        span {
          margin: 20px 0;
          font-size: 1.2em;
        }
      }
    }

    .arrow {
      padding: 30px 18px;
      color: #fff;
      position: absolute;
      top: 50%;

      .icon {
        font-size: 0.6em;
      }

      &.left {
        background-color: #a691b2;
        left: 0;
      }

      &.right {
        background-color: #a375ac;
        right: 0;
      }
    }
  }
}
</style>

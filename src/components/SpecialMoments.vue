<template>
  <div id="special_moments">
    <h6>Corporate & Weddings </h6>
    <h1>Baking Special Moments</h1>
    <div class="photo_container">
      <img src="../assets/corporate-bg.jpg" alt="">
      <img class="hidden" src="../assets/corporate-hover-bg.jpg" alt="">
      <div class="hidden text">
        <h6>International Bakery</h6>
        <h1>Corporate Events</h1>
        <button>Explore more</button>
      </div>
    </div>
    <div class="photo_container">
      <img src="../assets/wedding-bg.jpg" alt="">
      <img class="hidden" src="../assets/wedding-hover-bg.jpg" alt="">
      <div class="hidden text">
        <h6>Private Dining Hall</h6>
        <h1>Weddings & Parties</h1>
        <button>Explore more</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SpecialMoments'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#special_moments {
  text-align: center;
  display: flex;
  flex-wrap: wrap;

  h6, h1 {
    width: 100%;
    margin: 15px 0;
  }

  h6 {
    color: #c1c1c7;
    text-transform: uppercase;
    font-weight: 400;
  }

  h1 {
    color: #5b2ca2;
  }

  .photo_container {
    margin: 15px auto;
    width: 50%;
    position: relative;
  
    img {
      width: calc(100% - 100px);
      height: 800px;
      object-fit: cover;
      object-position: left;
    }

    .text {
      color: #fff;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      h1 {
        color: inherit;
        font-size: 2em;
        margin: 40px 0;

      }

      button {
        padding: 10px 15px;
      }
    }

    .hidden {
      display: none;
    }

    &:hover img {
      display: none;
    }

    &:hover .hidden {
      display: inline-block;
    }
  }
}
</style>

<template>
  <div id="special_moments">
    <h6>Corporate & Weddings </h6>
    <h1>Baking Special Moments</h1>
    <div class="photo_container first">
      <img src="../assets/corporate-bg.jpg" alt="">
      <img class="hidden" src="../assets/corporate-hover-bg.jpg" alt="">
      <div class="hidden text">
        <h6>International Bakery</h6>
        <h1>Corporate Events</h1>
        <div class="btn dark">Explore more</div>
      </div>
    </div>
    <div class="photo_container">
      <img src="../assets/wedding-bg.jpg" alt="">
      <img class="hidden" src="../assets/wedding-hover-bg.jpg" alt="">
      <div class="hidden text">
        <h6>Private Dining Hall</h6>
        <h1>Weddings & Parties</h1>
        <div class="btn dark">Explore more</div>
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
  justify-content: space-between;

  h6, h1 {
    width: 100%;
  }

  h6 {
    color: #818085;
    text-transform: uppercase;
    font-weight: 400;
    margin-bottom: 20px;
  }

  h1 {
    color: #5b2ca2;
  }

  .photo_container {
    margin: 0 auto;
    margin-top: 60px;
    width: calc(50% - 50px);
    position: relative;

    &.first {
      margin-right: 100px;
    }
  
    img {
      width: 100%;
      height: 840px;
      object-fit: cover;
      object-position: left;

      &.hidden {
        object-position: right;
      }
    }

    .text {
      color: #fff;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      h6 {
        color: #d3d3d3;
      }

      h1 {
        color: inherit;
        font-size: 2em;
        margin: 40px 0;
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

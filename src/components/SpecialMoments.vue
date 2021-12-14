<template>
  <div id="special_moments">
    <h6>Corporate & Weddings </h6>
    <h1>Baking Special Moments</h1>
    <div class="photo_container">
      <img src="../assets/corporate-bg.jpg" alt="">
    </div>
    <div class="photo_container">
      <img src="../assets/wedding-bg.jpg" alt="">
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
  
    img {
      width: calc(100% - 100px);
      height: 800px;
      object-fit: cover;
      object-position: left;
    }
  }
}
</style>

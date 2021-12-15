<template>
  <section id="social_container">
    <div class="social_card">
      <img src="../assets/social-1.jpg" alt="">
    </div>
    <div class="social_call">
      <h6>Made for Sharing</h6>
      <h1>Let's stay in touch</h1>
      <div class="btn dark">
        <i class="fab fa-instagram"></i>
          Follow Us
      </div>
    </div>
    <div class="social_card">
      <img src="../assets/social-2.jpg" alt="">
    </div>
    <div class="social_card">
      <img src="../assets/social-3.jpg" alt="">
    </div>
    <div class="social_card">
      <img src="../assets/social-5.jpg" alt="">
    </div>
    <div class="social_card">
      <img src="../assets/social-4.jpg" alt="">
    </div>
    <div class="social_card">
      <img src="../assets/social-6.jpg" alt="">
    </div>
  </section>
</template>

<script>
export default {
  name: 'Social'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#social_container {
  width: 90%;
  margin: 0 auto;
  height: 100vh;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  .social_card {
    width: calc(100% / 4 - 30px);
    height: calc(50% - 20px);
    margin: 0 5px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  .social_call {
    width: calc(100% / 2 - 20px);
    margin: 0 5px;
    background-color: rgba(189, 162, 243, 0.15);
    text-align: center;

    h6 {
      color: #c1c1c7;
      text-transform: uppercase;
      font-weight: 400;
      margin-top: 150px;
    }

    h1 {
      color: #5b2ca2;
      font-size: 2em;
      margin: 20px 0;
    }
  }
}
</style>

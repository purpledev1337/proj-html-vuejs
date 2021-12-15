<template>
  <section id="locations_container">
    <h6>Locations</h6>
    <h1>Visit our Bakeries</h1>
    <div class="location_card newyork_info">
      <div class="location_photo">
        <img src="../assets/new-york-bk.jpg" alt="">
      </div>
      <div class="location_info">
        <h1>New York</h1>
        <div class="info_text">
          <h6>
            Call Us
          </h6>
          <span>
            1.800.458.556
          </span>
        </div>
        <div class="info_text">
          <h6>
            Open All Week
          </h6>
          <span>
            9:00 AM - 6:00 PM
          </span>
        </div>
        <div class="btn light">View Map</div>
      </div>
    </div>
    <div class="location_card london_info">
      <div class="location_photo">
        <img src="../assets/london-bk.jpg" alt="">
      </div>
      <div class="location_info">
        <h1>London</h1>
        <div class="info_text">
          <h6>
            Call Us
          </h6>
          <span>
          1.800.458.556
          </span>
        </div>
        <div class="info_text">
          <h6>
            Open All Week
          </h6>
          <span>
            9:00 AM - 6:00 PM
          </span>
        </div>
        <div class="btn light">View Map</div>
      </div>
    </div>

  </section>
</template>

<script>
export default {
  name: 'Locations'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#locations_container {
  height: 100vh;
  text-align: center;
  display: flex;
  flex-wrap: wrap;

  h6, h1 {
    width: 100%;
  }

  h6 {
    color: #c1c1c7;
    text-transform: uppercase;
  }

  h1 {
    color: #5b2ca2;
    font-size: 2em;
  }

  .location_card {
    width: 50%;

    .location_photo {

      img {
        width: 100%;
        height: 100%;
        object-fit: contain;
      }
    }

    &.newyork_info {
      background-color: #0a5d6c15;
    }

    &.london_info {
      background-color: #f0caa136;
    }

    .location_info {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      padding: 20px 0;

      .info_text {
        color: #808080;

        span {
          font-weight: 500;
        }
      }

      h1 {
        margin: 20px 0;
      }

      h6 {
        text-transform: uppercase;
        margin: 20px 0;
      }
    }

  }
}
</style>

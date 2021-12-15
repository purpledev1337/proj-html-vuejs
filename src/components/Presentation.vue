<template>
  <div id="presentation">
    <div class="presentation_card first">
      <div class="background_overlay">
        <h1>Tell us what you have in mind</h1>
        <span>01</span>
        <div class="text_container">
          <h6>Manual Ingredients Selection</h6>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto fugit quas mollitia impedit minima qui, beatae eum repudiandae excepturi nisi accusantium, adipisci illo neque veritatis eos tempore soluta quod reiciendis.</p>
        </div>
      </div>
    </div>
    <div class="presentation_card second">
      <div class="background_overlay">
        <h1>We Start Baking</h1>
        <span>02</span>
        <div class="text_container">
          <h6>Sweet & Delicious</h6>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto fugit quas mollitia impedit minima qui, beatae eum repudiandae excepturi nisi accusantium.</p>
        </div>
      </div>
    </div>
    <div class="presentation_card third">
      <h6>Dont Just Take Our Word For It</h6>
      <h1>"Finally found an alternative to the mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity."</h1>
      <h6>Rachel Cooper, Founder</h6>
    </div>
    <div class="presentation_card fourth">
      <div class="background_overlay">
        <h1>Delivered to your home</h1>
        <span>03</span>
        <div class="text_container">
          <h6>Baked to order & gift wrapped</h6>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Architecto fugit quas mollitia impedit minima qui, beatae eum repudiandae excepturi nisi accusantium, adipisci illo neque veritatis eos tempore soluta quod reiciendis.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Presentation'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#presentation {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  .presentation_card {
    width: 100%;
    height: calc(100vh - 150px);
    margin: 40px 0;
    background-size: cover;
    display: flex;
    flex-wrap: wrap;
    position: relative;

    .background_overlay {
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.35);
      padding: 80px;

      .text_container {
      width: 35%;
      position: absolute;
      bottom: 100px;
      line-height: 2em;

        h6 {
          color: #d3d3d3;
          font-size: 0.8em;
        }

        p {
          color: #fff;
          font-size: 1.5em;
          margin-top: 25px;
        }
      }
    }

    h1 {
      color: #fff;
      font-size: 3.5em;
    }

    span {
      color: #fff;
      font-size: 6em;
      position: absolute;
      top: 100px;
      right: 100px;
    }

    h6 {
      color: #959595;
      text-transform: uppercase;
      font-weight: 400;
    }
  
    &.first {
      background-image: url("../assets/bakery-process-1.jpg");

      h1 {
        width: 40%;
      }

      .text_container {
        right: 50px;
      }
    }
  
    &.second {
      width: calc(50% - 20px);
      background-image: url("../assets/bakery-process-2.jpg");

      span {
      top: 60px;
      right: 80px;
      }

      .text_container {
        width: 50%;
      }
    }
  
    &.third {
      width: calc(50% - 20px);
      background-color: rgba(189, 162, 243, 0.15);
      padding: 80px;

      h1 {
        color: #5b2ca2;
        font-size: 3em;
        margin: 20px 0;
      }

      p {
        position: static;
      }
    }
  
    &.fourth {
      background-image: url("../assets/bakery-process-3.jpg");

      h1 {
        margin: 25px 0;
      }

      .text_container {
        width: 35%;
      }
    }
  }

}
</style>

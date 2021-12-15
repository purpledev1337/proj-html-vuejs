<template>
  <footer>
    <section id="jumbotron_container">
      <div id="jumbotron">
        <h6>Try Our Seasonal Products</h6>
        <h1>Order for pick-up or delivery to your home</h1>
        <div class="btn light">Shop Now</div>
      </div>
    </section>
    <nav>
      <section id="nav_left">
        <img src="../assets/avada-bakery-logo-retina.png" alt="">
        <ul>
          <NavigationBarLink
          class="nav_link"
          v-for="link, i in linkData" :key="i"
          :linkText="link.text"
          :linkUrl="link.url"
          />
          <li class="nav_link">
            <a href="#">
              <div>
                Orders
              </div>
            </a>
          </li>
          <li class="nav_link">
            <a href="#">
              <div>
                <font-awesome-icon class="icon" :icon="['fas', 'shopping-cart']"/>
              </div>
                <span>0</span>
            </a>
          </li>
        </ul>
        <p>&copy; Copyright 2021 - 2022 | Bakery Theme by purpledev1337 | All Rights Reserved | Powered by Vue CLI 4.5.0 - Vue JS 2.6.11</p>
      </section>
      <section id="nav_right">
        <h1>Subscribe to our Newsletter</h1>
        <input type="email" placeholder="Enter email address*">
        <div class="btn dark">Subscribe</div>
        <div id="social_icons">
          <a href="">
            <i class="fab fa-instagram"></i>
          </a>
          <a href="">
            <i class="fab fa-twitter"></i>
          </a>
          <a href="">
            <i class="fab fa-facebook-f"></i>
          </a>
          <a href="">
            <i class="fab fa-pinterest-p"></i>
          </a>
        </div>
      </section>
    </nav>
  </footer>
</template>

<script>
import NavigationBarLink from './NavigationBarLink.vue'

export default {
  name: 'Footer',
  components: {
    NavigationBarLink
  },
  props: {
    linkData : Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
footer {

  #jumbotron_container {
    width: 100%;
    height: 550px;
    position: relative;
    background-image: url("../assets/call-to-action-bg.jpg");
    background-size: cover;
    background-position: center;
    padding: 100px 300px;

    #jumbotron {
      width: 60%;
      height: 80%;
      margin-left: 50px;

      h6 {
        color: #b1b9bf;
        text-transform: uppercase;
      }

      h1 {
        font-size: 2.7em;
        color: #fff;
        margin: 30px 0;
      }

      .btn {
        margin-top: 50px;
        font-weight: 200;
        font-size: 1.2em;
        padding: 15px 40px;
      }
    }
  }

  nav {
    width: 90%;
    height: 450px;
    margin: 0 auto;
    padding: 50px 0;
    
    #nav_left {
      width: 50%;
      float: left;

      img {
        height: 80px;
        margin-top: 20px;
      }

      ul {
        width: 90%;
        display: flex;
        justify-content: space-between;
        margin: 50px 0;

        .nav_link {

          a {

            div {
              padding: 6px 0;
              display: inline-block;
            }
            span {
              font-size: 1.2em;
              background-color: rgba(189, 162, 243, 0.3);
              border: 4px solid transparent;
              border-radius: 50%;
              padding: 0 5px;
              margin: 0 5px;
            }
          }
        }
      }

      p {
        font-size: 0.8em;
        color: #818085;
        margin-top: 120px;
      }
    }

    #nav_right {
      width: 50%;
      float: right;
      text-align: right;

      h1 {
        color: #5b2ca2;
        font-size: 1.4em;
        margin-top: 30px;
      }

      input {
        width: 50%;
        height: 40px;
        margin: 50px 0;
        margin-right: 15px;
        border: 1px solid #8180852d;
        padding: 25px 15px;
        font-size: 1em;
      }

      #social_icons {

        margin-top: 100px;

        i {
          width: 60px;
          font-size: 1.2em;
        }
      }
    }
  }
}


</style>

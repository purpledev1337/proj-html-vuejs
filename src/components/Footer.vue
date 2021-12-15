<template>
  <footer>
    <section id="jumbotron_container">
      <div id="jumbotron">
        <h6>Try Our Seasonal Products</h6>
        <h1>Order for pick-up or delivery to your home</h1>
        <button>Shop Now</button>
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
        <p>&copy; Copyright 2021 - 2022 | Bakery Theme by purpledev1337 | All Rights Reserved | Powered by VueJS 2.6.11 </p>
      </section>
      <section id="nav_right">
        <h1>Subscribe to our Newsletter</h1>
        <input type="email" placeholder="Enter email address*">
        <button>Subscribe</button>
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
    height: 480px;
    position: relative;
    background-image: url("../assets/call-to-action-bg.jpg");
    background-size: cover;
    background-position: center;
    padding: 100px 300px;

    #jumbotron {
      width: 60%;
      height: 80%;

      h6 {
        color: #c1c1c7;
        text-transform: uppercase;
      }

      h1 {
        font-size: 3em;
        color: #fff;
        margin: 20px 0;
      }

      button {
        margin-top: 50px;
        padding: 10px;
      }
    }
  }

  nav {
    
    #nav_left {
      width: 50%;
      padding: 50px;
      float: left;

      img {
        height: 80px;
      }

      ul {
        display: flex;
        justify-content: space-between;
        margin: 70px 0;

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
        color: #c1c1c7;
      }
    }

    #nav_right {
      width: 50%;
      padding: 50px;
      float: right;
      text-align: right;

      h1 {
        color: #5b2ca2;
        font-size: 1.8em;
      }

      input {
        width: 50%;
        height: 40px;
        margin: 50px 0;
        margin-right: 15px;
      }

      button {
        padding: 10px;
      }

      #social_icons {
        margin-top: 100px;

        i {
          width: 60px;
          font-size: 1.2em;
          // font-weight: 600;
        }
      }
    }
  }
}


</style>

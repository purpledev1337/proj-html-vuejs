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
            <a href="#">Orders</a>
          </li>
          <li class="nav_link">
            <a href="#">
              <font-awesome-icon class="icon" :icon="['fas', 'shopping-cart']"/>
              <span>0</span>
            </a>
          </li>
        </ul>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellat labore ex corrupti qui quo! Dicta eligendi aut eum hic quo blanditiis, aspernatur harum voluptatum perferendis. Delectus neque deserunt sed fuga?</p>
      </section>
      <section id="nav_right">
        <h1>Subscribe to our Newsletter</h1>
        <input type="email" placeholder="Enter email address*">
        <button>Subscribe</button>
        <div id="social_icons">
          <a href="">
            <font-awesome-icon icon="hashtag" />
          </a>
          <a href="">
            <font-awesome-icon icon="hashtag" />
          </a>
          <a href="">
            <font-awesome-icon icon="hashtag" />
          </a>
          <a href="">
            <font-awesome-icon icon="hashtag" />
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
        margin: 50px 0;
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

        .icon {
          width: 50px;
        }
      }
    }
  }
}


</style>

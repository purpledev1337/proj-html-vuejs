<template>
  <header>
    <nav>
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
              My Account
            </a>
          </li>
          <li class="nav_link">
            <a href="#">
              <font-awesome-icon class="icon" :icon="['fas', 'shopping-cart']"/>
            </a>
          </li>
      </ul>
    </nav>
    <div id="jumbotron">
      <h6>Fresh & Tasty Bakery Every Day</h6>
      <h1>The Perfect Fresh Bread</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, pariatur itaque! Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <button>Explore our products</button>
    </div>
  </header>
</template>

<script>
import NavigationBarLink from './NavigationBarLink.vue'

export default {
  name: 'Header',
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
header {
  height: 100vh;
  background-image: url("../assets/hero-header-bakery.jpg");
  background-size: cover;
  position: relative;

  nav {
    height: 120px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
      height: 90px;
    }
 
    ul {
      display: flex;
      justify-content: space-between;

      .icon {
        color: #5b2ca2;
        padding: 2px;
      }
    }
  }

  #jumbotron {
    width: 30%;
    position: absolute;
    top: 40%;
    left: 5%;

    h6 {
      text-transform: uppercase;
      color: #929295;
    }

    h1 {
      font-size: 3.5em;
      color: #5b2ca2;
      margin: 25px 0;
    }

    button {
      margin-top: 30px;
      padding: 10px;
    }
  }
}
</style>

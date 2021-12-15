<template>
  <header>
    <nav>
      <img src="../assets/avada-bakery-logo-retina.png" alt="">
      <ul>
          <li class="nav_link">
            <a class="active" href="#">
              <div>
                Home
              </div>
            </a>
          </li>
          <NavigationBarLink
          class="nav_link"
          v-for="link, i in linkData" :key="i"
          :linkText="link.text"
          :linkUrl="link.url"
          />
          <li class="nav_link">
            <a href="#">
              <div>
                My Account
              </div>
            </a>
          </li>
          <li class="nav_link">
            <a href="#">
              <div>
                <font-awesome-icon class="icon" :icon="['fas', 'shopping-cart']"/>
              </div>
            </a>
          </li>
      </ul>
    </nav>
    <div id="jumbotron">
      <h6>Fresh & Tasty Bakery Every Day</h6>
      <h1>The Perfect Fresh Bread</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, pariatur itaque! Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <div class="btn light">Explore our products</div>
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
      margin: 0 25px;
      height: 100px;
    }
 
    ul {
      width: 40%;
      display: flex;
      justify-content: space-around;

      .nav_link {
        font-size: 0.8em;
        text-transform: uppercase;

        a {

          &.active {

            div {
              padding: 6px 0;
              border-bottom: 2px solid #5b2ca2;
            }
          }

          div {
            padding: 6px 0;
          }
        }
      }

      .icon {
        color: #5b2ca2;
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

    p {
      color: #959595;
      font-size: 1.3em;
      line-height: 30px;
    }
  }
}
</style>

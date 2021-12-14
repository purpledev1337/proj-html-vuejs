<template>
  <div id="app">
    <ul>
      <li>
    <Header
    :linkData="links"/>
      </li>
      <li>
    <Main/>
      </li>
      <li>
    <Footer
    :linkData="links"/>
      </li>
    </ul>


  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      links: [
        {
          text: "Shop",
          url: "#"
        },
        {
          text: "About",
          url: "#"
        },
        {
          text: "Gallery",
          url: "#"
        },
        {
          text: "Locations",
          url: "#"
        },
        {
          text: "Journal",
          url: "#"
        },
        {
          text: "Contact",
          url: "#"
        }
      ]
    }
  }
}
</script>

<style lang="scss">

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.nav_link {
  list-style: none;
  padding: 20px;

  a {
    text-decoration: none;
  }
}

</style>

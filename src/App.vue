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
@import url('https://fonts.googleapis.com/css2?family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400;1,700;1,900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif;
}

h1, h2, h3 {
  font-family: 'Merriweather', sans-serif;
  font-weight: 800;
}

.nav_link {
  list-style: none;

  a {
    text-decoration: none;
  }
}

</style>

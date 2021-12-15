<template>
  <div>
    <Header
    :linkData="links"/>

    <div id="main_container">
      <Main/>
    </div>

    <Footer
    :linkData="links"/>
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

#main_container {
  width: 90%;
  margin: 0 auto;
}

h1, h2, h3 {
  font-family: 'Merriweather', sans-serif;
  font-weight: 800;
}

h6 {
  letter-spacing: 3px;
}

.btn {
  display: inline-block;
  margin-top: 30px;
  padding: 15px 35px;
  border-radius: 5px;
  font-size: 0.8em;
  font-weight: 600;

  &.light {
    background-color: #fff;
    color: #5b2ca2;

    &:hover {
      background-color: #5b2ca2;
      color: #fff;
    }
  }
  
  &.dark {
    background-color: #5b2ca2;
    color: #fff;

    &:hover {
    background-color: #e6ddf8;
    color: #5b2ca2;
    }
  }

  &:hover {
    cursor: pointer;
  }
}

.nav_link {
  list-style: none;
  letter-spacing: 2px;

  a {
    text-decoration: none;
  }
}

</style>

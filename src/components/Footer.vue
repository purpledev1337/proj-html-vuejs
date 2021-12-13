<template>
  <div>
    FOOTER_____
    <section>
      Jumbotron (static)
    </section>
    <nav>
      IMG logo <br>
      <ul>
        <li v-for="link, i in links" :key="i">
          <a :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
      <section>
        NewsLetter subscription
      </section>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      links: [
        {
          text: "Link Footer 1",
          url: "#",
          here: true
        },
        {
          text: "Link Footer 2",
          url: "#",
          here: false
        },
        {
          text: "Link Footer 3",
          url: "#",
          here: false
        },
        {
          text: "Link Footer 4",
          url: "#",
          here: false
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

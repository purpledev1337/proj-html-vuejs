<template>
  <div>
    HEADER_____
    <nav>
      IMG logo <br>
      Nav printed with v-for
    </nav>
    <section>
      Jumbotron (static)
    </section>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      links: [
        {
          text: "Link Header 1",
          url: "#",
          here: true
        },
        {
          text: "Link Header 2",
          url: "#",
          here: false
        },
        {
          text: "Link Header 3",
          url: "#",
          here: false
        },
        {
          text: "Link Header 4",
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

<template>
  <div>
    <li>
      <a :href="linkUrl">
        <div>
          {{ linkText }}
        </div>
      </a>
    </li>
  </div>
</template>

<script>
export default {
  name: 'NavigationBarLink',
  props: {
    linkText: String,
    linkUrl: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
a {
  
  div {
    padding: 6px 0;
  }
}
</style>

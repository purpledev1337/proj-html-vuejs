<template>
  <div>
    <li>
      <a :href="linkUrl"> {{ linkText }} </a>
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

</style>

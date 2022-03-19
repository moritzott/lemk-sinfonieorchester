<template>
  <nav class="navbar-desktop">
      <Navigation />
  </nav>
</template>

<script>
import Navigation from './Navigation.vue'

export default {
    components: {
        Navigation
    }
}
</script>

<style scoped>

    nav {
        float: right;
        margin-right: 3em;
    }

</style>
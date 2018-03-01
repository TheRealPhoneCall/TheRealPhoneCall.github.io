<template>
  <v-container>
    <about-avatar></about-avatar>
    <br/>
    <br/>
    <portfolio></portfolio>
    <blog></blog>
  </v-container>
</template>

<script>
  import AboutAvatar from '../subcomponents/AboutAvatar'
  import Portfolio from '../subcomponents/Portfolio'
  import Blog from '../subcomponents/Blog'

  export default {
    components: {
      AboutAvatar, Portfolio, Blog,
    },

  }
</script>

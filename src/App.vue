<template>
  <v-app light>
    <app-header />
    <app-content />
    <app-footer />
  </v-app>
</template>

<script>
  import AppHeader from './components/layout/AppHeader'
  import AppContent from './components/layout/AppContent'
  import AppFooter from './components/layout/AppFooter'

  export default {
    components: {
      AppHeader, AppContent, AppFooter
    },
    data: () => ({
      title: 'TheReal PhoneCall',
      avatar: {
        size: '200px',
        tile: false
      }
    })
  }
</script>

<style lang="stylus">
  @import './stylus/vuetify'
</style>


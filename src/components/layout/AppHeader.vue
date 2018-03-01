<template>
  <v-toolbar dark extended>
    <v-toolbar-title v-text="title"></v-toolbar-title>
    
    <v-toolbar-items class="hidden-xs-only" slot="extension">
      <v-btn
          flat
          v-for="item in menuItems"
          :key="item.title"
          :to="item.link"
        >
        {{ item.title }}
      </v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  data: () => ({
    title: 'TheReal PhoneCall',
    menuItems: [
      {title: 'About', link: `#about`},
      {title: 'Portfolio', link: `#portfolio`},
      {title: 'Blog', link: `#blog`},
      {title: 'Contact', link: `#contact`}
    ]
  })
}
</script>

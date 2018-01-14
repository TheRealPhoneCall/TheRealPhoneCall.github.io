<template>
  <v-toolbar dark>
    <v-toolbar-title v-text="title"></v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-xs-only">
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

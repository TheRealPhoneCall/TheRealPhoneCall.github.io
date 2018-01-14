<template>
  <section>
    <v-layout row>
      <v-flex xs4 class="text-xs-right">
        <v-avatar
          :tile="tile"
          :size="size"
          class="grey mr-5"
        >
          <img src="../../assets/profile/DarylBig.png" alt="avatar">
        </v-avatar>
      </v-flex>
      <v-flex xs8>
        <p class="display-2">Hi, I'm {{ fullName }}</p>
        <p class="subheading">A software engineer, cajon maker and a drummer.</p>
        <p class="subheading">I enjoy writing code. I can write web apps based in Django and Node. I'm a fullstack developer and I can figure my way around the backend and frontend of the project. My frameworks are django and node in the backend and react and vue in the front.</p>
        <p class="subheading">Desktop and mobile apps writen in javascript are my thing recently too! So projects in these platforms are all welcome!</p>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
  export default {
    data: () => ({  
      fullName: 'Daryl Pongcol',
      size: '200px',
      tile: false      
    })
  }
</script>

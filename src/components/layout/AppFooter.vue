<template>
  <v-footer class="blue-grey lighten-1">
    <section>
      <v-container grid-list-xl>
        <v-layout row wrap justify-center class="my-5">
          <v-flex xs12 sm6>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">Personal Info</div>
              </v-card-title>
              <v-card-text>
                Graduated Electronics Engineering at Mindanao State University - Iligan Institute of Technology. Currently finishing MS degree in Computer Applications. A freelance fullstack web developer. 
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">Contact Me</div>
              </v-card-title>
              <v-list class="transparent">
                <v-list-tile 
                  v-for="contact in contactMeList" 
                  :key="contact.id"
                >
                  <v-list-tile-action>
                    <v-icon class="blue--text text--lighten-2">{{contact.icon}}</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>{{contact.data}}</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>                
              </v-list>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </section>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      contactMeList: [
        {id: 0, icon: 'phone', data: '+63917 150 1005'},
        {id: 1, icon: 'place', data: 'Iligan City, Philippines'},
        {id: 2, icon: 'email', data: 'pongcoldaryl@gmail.com'}
      ]
    })
  }
</script>
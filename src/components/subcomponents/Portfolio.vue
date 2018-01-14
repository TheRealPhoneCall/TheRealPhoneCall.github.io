<template>
  <section>
    <v-layout row>
      <v-flex 
        xs12 md6 
        class="text-xs-left mr-3"
        v-for="project in portfolio"
        :key="project.id"
        >
        <v-card>
          <!-- <v-card-media
            class="white--text"
            height="200px"
            :src="loadPortfolioImg(project)"
          /> -->
          <v-card-media
            class="white--text"
            height="200px"
            :src="`../../assets/Portfolio/${project.title}/${project.img}`"
          />
          <v-card-title>
            <div>
              <span class="grey--text">{{ project.title }}</span><br>
              <span>{{ project.description }}</span>
              <v-spacer/>
              <v-chip v-for="tech in project.stack" :key="tech.name">
                <v-avatar>
                  <!-- <img :src="loadStackImg(tech.avatar)"> -->
                  <img :src="`../../assets/stack/${tech.avatar}`">
                </v-avatar>
                {{ tech.name }}
              </v-chip>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-btn flat color="orange">More Info</v-btn>
            <v-btn flat color="orange">Source Code</v-btn>
            <v-btn 
              flat 
              color="orange" 
              v-if="project.website" 
              to="app.soamanager.com.au"
            >Website</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
// import imgMixin from '../mixins/imgMixin'

export default {
  data: () => ({
    portfolio: [
      {id: 0, title: 'SoA Manager', img: 'dashboard.JPG', website: 'app.soamanager.com.au', 
       stack: [
         {name: 'vue', avatar: 'vue.png'},
         {name: 'django', avatar: 'django.png'}
       ]
      },
      {id: 1, title: 'berdperc', img: 'vue_dashboard.PNG', imgMobile: 'vue_mobile.PNG',
       stack: [
         {name: 'vue', avatar: 'vue.png'},
         {name: 'react', avatar: 'react.png'},
         {name: 'node', avatar: 'node.png'},
         {name: 'python', avatar: 'python.png'}
       ]
      },
      {id: 2, title: 'SoA Manager', img: 'dashboard.JPG', website: 'app.soamanager.com.au', 
       stack: [
         {name: 'vue', avatar: 'vue.png'},
         {name: 'django', avatar: 'django.png'}
       ]
      },
      {id: 3, title: 'berdperc', img: 'vue_dashboard.PNG', imgMobile: 'vue_mobile.PNG',
       stack: [
         {name: 'vue', avatar: 'vue.png'},
         {name: 'react', avatar: 'react.png'},
         {name: 'node', avatar: 'node.png'},
         {name: 'python', avatar: 'python.png'}
       ]
      }
    ]
  }),
  // mixins: [imgMixin]
}
</script>

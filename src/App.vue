<template>
  <v-app>
    <navBar/> 
    <v-content>
      <Homepage/>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>Loretta Thompson Smells!!! &copy; 2018</span>
    </v-footer>
  </v-app>
</template>

<script>
import Homepage from './Views/Homepage.vue'
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    Homepage,
    NavBar
  },
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

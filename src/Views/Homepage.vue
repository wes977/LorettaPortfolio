<template>
  <v-container fluid grid-list-md >
      <v-layout column justify-space-between >
        <v-flex>
          <v-layout row wrap align-content-start>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="3"/>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="2"/>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="3"/>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="2"/>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="3"/>
<ProjectTile v-bind:tileSize="1"/>
<ProjectTile v-bind:tileSize="2"/>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>


</template>

<script>
import ProjectTile from '../components/ProjectTile.vue'
export default {
  name: 'Homepage',
  components: {ProjectTile},
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

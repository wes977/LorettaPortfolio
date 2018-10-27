<template>
    <v-flex d-flex xs6 sm6 md3 lg3 v-if="this.tileSize == 1 ">
        <v-card :hover="true" tile flat height="100%" class="ProjectBoxContainer">

                <img src="../assets/old-milwaukee.png" alt="Avatar" class="image" style="width:100%">
                <div class="middle">
                    <div class="text">Cold Milwaukee</div>
                </div>

        </v-card>
    </v-flex>
        <v-flex d-flex xs12 sm12 md6 lg6 v-else-if="this.tileSize == 2">
        <v-card :hover="true" tile flat class="ProjectBoxContainer">
                <img src="../assets/mobile_About.jpg" alt="Avatar" class="image" style="width:100%">
                <div class="middle">
                    <div class="text">Cold Milwaukee</div>
            </div>
        </v-card>
    </v-flex>
            <v-flex d-flex xs6 sm6 md3 lg3 v-else-if="this.tileSize == 3">
        <v-card :hover="true" tile flat class="ProjectBoxContainer">
                            <img src="../assets/OldMillCan.png" alt="Avatar" class="image" style="width:100%">
                <div class="middle">
                    <div class="text">Cold Milwaukee</div>
                </div>
        </v-card>
    </v-flex>
</template>

<script>
export default {
  name: 'ProjectTile',
  props: {
    msg: String,
    tileSize: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.DisplayCard,
.InfoCard {
  width: 100%;
  height: 100%;
  position: relative;
  top: 0;
  left: 0;
}
.InfoCard {
    opacity: 0;
  width: 100%;
  height: 100%;
  display: none;
  z-index: 30;
  background-color: transparent; 
      -moz-transition: opacity .75s ease-in-out;
    -o-transition: opacity .75s ease-in-out;
    -webkit-transition: opacity .75s ease-in-out;
    transition: opacity .75s ease-in-out;
}

.DisplayCard {


   background: #fff;
    transition: thing 5s ;
    -moz-transition: thing 5s ;
    -o-transition: thing 5s ;
    -webkit-transition: thing 5s ;
    
    background: #fff;

}
.DisplayCard img {
    background-color: transparent;
    height:auto;
    max-height: 250px;
}
.DisplayCard:hover {
        z-index: 0;
        opacity: 0.25;
}
.InfoCard:hover {
opacity: 1;
}


.ProjectBoxContainer {
    position: relative;
    width: 100%;
        height: 100%;
    max-height: 250px;
}

.image {
  opacity: 1;
  display: block;
  width: 100%;
  height: auto;
  transition: .5s ease;
  backface-visibility: hidden;
      max-height: 250px;
}

.middle {
    transition: .5s ease;
    opacity: 0;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    text-align: center;
}

div.ProjectBoxContainer:hover img.image {
  opacity: 0.3;
}

.ProjectBoxContainer:hover .middle {
    opacity: 1;
    width: 100%;
    height: 100%;
}

.text {
    background-color: #4CAF50;
    color: white;
    font-size: 16px;
    padding: 16px 32px;
    height: 100%;
    opacity: 0.6;
}


</style>

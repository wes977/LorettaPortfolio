<template>
    <v-flex d-flex xs6 sm6 md3 lg3 v-if="this.tileSize == 1 ">
        <v-card :hover="true" tile flat height="100%" >
            <div class="DisplayCardContainer">
            <div class="InfoCard">This is a TEST</div>
            <div class="DisplayCard">
                <img src="../assets/old-milwaukee.png" alt="Smiley face" height="auto" width="100%"> 
            </div>
            </div>
        </v-card>
    </v-flex>
        <v-flex d-flex xs12 sm12 md6 lg6 v-else-if="this.tileSize == 2">
        <v-card :hover="true" tile flat >
            <div class="DisplayCard">
                <img src="../assets/mobile_About.jpg" alt="Smiley face" height="auto" width="100%"> 
            </div>
        </v-card>
    </v-flex>
            <v-flex d-flex xs6 sm6 md3 lg3 v-else-if="this.tileSize == 3">
        <v-card :hover="true" tile flat >
            <div class="DisplayCard">
                <img src="../assets/OldMillCan.png" alt="Smiley face" height="auto" width="100%"> 
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
.DisplayCardContainer {
    
}

.DisplayCard,
.InfoCard {
  width: 100%;
  height: 100%;
  position: relative;
  top: 0;
  left: 0;
}
.InfoCard {
    opacity: 0.5;
  z-index: 10;
  width: auto;
  height: 100%;
  display: none;
}

.DisplayCard {
    opacity: 1;
    height: 100%;
    max-height: 250px;
   background: #fff;
    -moz-transition: all .2s ease-in;
    -o-transition: all .2s ease-in;
    -webkit-transition: all .2s ease-in;
    transition: all .2s ease-in;
    background: #fff;

}
.DisplayCard img {
    background-color: transparent;
    height:auto;
    max-height: 250px;
}
.DisplayCard:hover {
    background: rgb(231, 7, 7) !important;

}

@keyframes highlight {
 	0% {
 		background: red
 	}
 	100% {
 		background: red;
 	}
}

</style>

<template>
    <v-toolbar color="#a43cb5">
        <v-toolbar-title class="TitleWords" >Loretta</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
            <v-btn flat class="hvr-shutter-in-vertical ">About me</v-btn>
            <v-btn flat class="hvr-shutter-in-vertical ">Projects</v-btn>
            <v-btn flat class="hvr-shutter-in-vertical ">Contact</v-btn>
        </v-toolbar-items>
    </v-toolbar>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.TitleWords {
    color: white;
    text-shadow: 2px 2px 6px #000000;
}

/* Shutter In Vertical */
.hvr-shutter-in-vertical {
    color: white;
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  position: relative;
  background: #9c27b0;
  -webkit-transition-property: color;
  transition-property: color;
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  text-shadow: 2px 2px 4px #000000;
}
.hvr-shutter-in-vertical:before {
  content: "";
  position: absolute;
  z-index: -1;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: #e1e1e1;
  -webkit-transform: scaleY(1);
  transform: scaleY(1);
  -webkit-transform-origin: 50%;
  transform-origin: 50%;
  -webkit-transition-property: transform;
  transition-property: transform;
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-timing-function: ease-out;
  transition-timing-function: ease-out;
}
.hvr-shutter-in-vertical:hover, .hvr-shutter-in-vertical:focus, .hvr-shutter-in-vertical:active {
  color: white;
  text-shadow: 4px 4px 8px #000000;
}
.hvr-shutter-in-vertical:hover:before, .hvr-shutter-in-vertical:focus:before, .hvr-shutter-in-vertical:active:before {
  -webkit-transform: scaleY(0);
  transform: scaleY(0);
}
</style>

<template>
<Home first-name="Eduardo" last-name="Razo" otro="Algo"></Home>
</template>

<script>
import Home from "./components/Home.vue";
import {provide} from "vue";
//@ = carpeta source "src"

export default {
    name: "App",
    components: { Home },
    setup(){
      provide("username", "edracobi");
    }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.fade-enter-from,
.fade-leave-to{
  opacity: 0;
}

.fade-leave-active,
.fade-enter-active{
  transition: opacity 0.5s ease;
}
</style>

<template>
 <div>
 <div>{{ text }}</div>
 <div>{{ algo }}</div>
 </div>
</template>

<script>
//@ = carpeta source "src"
import base from '@/mixins/base';

export default {
  name: "App",
  mixins: [base],
  data(){
    return{
      text: "Hola Vue",
    };
  },
  //Funciones
  beforeCreate(){
    console.log("beforeCreate", this.$data, this.$el);
  },
  created(){
    console.log("created", this.$data, this.$el);
  },
  mounted(){
    console.log("mounted", this.$data, this.$el);
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

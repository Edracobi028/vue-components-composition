<template>
    <div>
        <button @click="toggle">Modal</button>
        <teleport to="body"></teleport>
        <div v-show="show" class="modal">
            <h1>Titulo</h1>
            <p>Lorem ipsum dolor </p>
            <button @click="toggle">Cerrar</button>
        </div> 
    </div>    
</template>

<script>
    export default{
        data(){
            return{
                show:false,
            }
        },
        methods:{
            toggle(){
               this.show = !this.show; //actualizar la variable show para saber si es verdadero o falso
            }
        }
    }
</script>
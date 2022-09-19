<template>
    <div>{{ fullName }}</div>
    <div>{{ username }}</div>
    <button ref="btn">Click!</button>
</template>

<script setup>
import { defineProps, defineExpose, ref, toRefs, computed, watch, inject } from 'vue';
        //Definimos los props
        const props = defineProps({ 
            firstName: String,
            lastName: String,
        });

        const{ firstName, lastName } = toRefs(props);

        const fullName = computed(() => {
            return `${firstName.value} ${lastName.value} `;
        });

        const username = inject("username");
        defineExpose({ 
            fullName,
        });

        expose({ fullName,});//Enviamos por funcion expose

        //para que sea reactiva se crea una variable por convencion null  y ponerla accesible en el return
        const btn = ref(null);

        watch(btn, (valor) => {
            console.log(valor);
        });
                
  
</script>
<template>
    <div>fullName: {{ fullName }}</div>
</template>

<script>
import { ref, computed } from 'vue';

    export default{
        setup() {
            const firstName = ref("Eduardo");
            const lastName = ref("Razo");

            const fullName = computed(() => {
                return `${firstName.value} ${lastName.value} `;
            });


            return{
                fullName,
            };
        },
    };
</script>
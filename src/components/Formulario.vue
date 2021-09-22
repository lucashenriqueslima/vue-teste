<template>
    <div>
        <form action="" @submit="enviaform($event)">
        <input type="text" v-model="name">
        <input type="text" v-model="profissao">
        <input-submit />
        </form>
    </div>
</template>

<script>
import InputSubmit from './forms/InputSubmit.vue'
import InputText from './forms/InputText.vue'
export default {
     name: 'Formulario',
    components: { InputText, InputSubmit },
    
    data() {
        return{
            name: "",
            profissao: ""
        }
    },
    
    methods: {
        enviaform(e){
            e.preventDefault();
            console.log("assda")
        }
    }
}
</script>
<template>
    <h1>TESTE LifeCycle: {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Matheus',
        }
    },
    created() {
        setTimeout(() =>{
        this.nome = 'Lucas'
        },1000)
        
    },
    mounted() {
        setTimeout(() =>{
        this.nome = 'Pedro'
        },2000)
    }
}
</script>
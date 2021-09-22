<template>
    <div>
        <h1>Teste</h1>
        <p>Meu nome é {{ nome }} e {{ idade }}</p>
    </div>
</template>

<script>
export default {
    name: 'PrimeiroComponente',
    data() {
        return{
            nome: 'Lucas',
            idade: '21',
        }
    }
}
</script>
<template>
<div>
    <info />
    <formulario />
</div>
</template>

<script>
import Info from './Info.vue'
import Formulario from './Formulario.vue'

export default {
    name: 'Pessoa',
    components: {
        Formulario,
        Info
    },
    data() {
        return {

        }
    }
}
</script>
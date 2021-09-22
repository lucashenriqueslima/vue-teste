<template>
    <div>
        <Picture />
        <p v-if="is_working">Está trabalhando</p>
        <p v-else>Não está trabalhando</p>
        <div>
            <button @click="showEmail">{{ button_title }}</button>
        </div>
        <p v-show="show_email">Email: lucas@a.com</p>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <p>Tecnologias backend utilizadas:</p>
        <ul>
            <li v-for="(tecnologis, index) in arr_backend" v-bind:key="index">{{ tecnologis }}</li>
        </ul>
        <p>Tecnologias front-end utilizadas:</p>
        <ul>
            <li v-for="tecnology in arr_frontend" :key="tecnology.id">
                {{ tecnology.language }}
            </li>
        </ul>

        <p>Acesse: <a href="teste">Clique Aqui</a></p>
    </div>
</template>

<script>
import Picture from './Picture.vue'
export default {
    name: 'Info',
    components: {
        Picture
    },
        data() {
        return {
            nome: 'Lucas',
            teste: 'http://www.google.com',
            is_working: false,
            show_email: false,
            button_title: "Mostrar Email",
            arr_backend: ['JavaScript', 'PHP', 'Java', 'Python'],
            arr_frontend: [
                {id: 1, language: "HTML"},
                {id: 2, language: "CSS"},
                {id: 3, language: "JS"}
            ]
        }
    },
    methods: {
        showEmail() {
            this.show_email = !this.show_email
            if(this.show_email){
                this.button_title = "Ocultar Email"
            }else{
                this.button_title = "Mostrar Email"
            }
        }
    }
}
</script>
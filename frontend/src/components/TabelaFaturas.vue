<template>
    <div v-if="listaFaturas != ''">
        <table class="table table-striped table-borderless">
            <thead>
                <tr>
                    <th scope="col">ID</th>
                    <th scope="col">Name</th>
                    <th scope="col">Price</th>
                    <th scope="col">Closes in</th>
                    <th scope="col">Status</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="listaFatura in listaFaturas" :key="listaFatura.id">
                    <th scope="row">{{ listaFatura.id }}</th>
                    <td>{{ listaFatura.nome_fatura }}</td>
                    <td>{{ listaFatura.preco }}</td>
                    <td>{{ listaFatura.fechamento }}</td>
                    <td>{{ listaFatura.status }}</td>
                </tr>
            </tbody>
        </table>
    </div>
    <div v-else>
        <h2>{{ error }}</h2>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    data(){
        return{
            listaFaturas: [],
            error: 'No data found...'
        };
    },

    mounted(){
        this.getListaFaturas();
    },

    methods: {
        getListaFaturas() {
            axios
                .get('http://localhost:8000/api/faturas')
                .then( response => {
                    this.listaFaturas = response.data
                })
                .catch( error => {
                    console.log(error);
                })
        }
    }
};
</script>

<style scoped>
</style>
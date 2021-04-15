<template>
    <table class="table table-striped table-borderless">
        <thead>
            <tr>
                <th scope="col">ID</th>
                <th scope="col">Nome</th>
                <th scope="col">Preço</th>
                <th scope="col">Fechamento em</th>
                <th scope="col">Ações</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="listaFatura in listaFaturas" :key="listaFatura.id">
                <th scope="row">{{ listaFatura.id }}</th>
                <td>{{ listaFatura.nome_fatura }}</td>
                <td>{{ listaFatura.preco }}</td>
                <td>{{ listaFatura.fechamento }}</td>
                <td></td>
            </tr>
        </tbody>
    </table>
</template>

<script>
export default {
    data(){
        return{
            listaFaturas: []
        };
    },
    mounted() {},
    methods: {
        getListaFaturas() {
            // axios
            // .get()
        }
    },
}
</script>

<style scoped>
</style>
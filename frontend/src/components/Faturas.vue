<template>
    <div class="container">
        <div class="logo">
            <div class="row justify-content-md-center">
                <img src="../assets/logo_colorido_stroke.svg" />
            </div>
            <div class="row">
                <p>{{ title }}</p>
            </div>
        </div>
        <div class="box">
            <div class="row">
                <div class="col-6">
                    <h2>{{ tableName }}</h2>
                </div>
                <div class="col-6">
                    <BotoesExportacao />
                </div>
            </div>

            <TabelaFaturas />
        </div>
        <Footer />
    </div>
</template>

<script>
import BotoesExportacao from '../components/BotoesExportacao.vue'
import TabelaFaturas from '../components/TabelaFaturas.vue'
import Footer from '../components/Footer.vue'

export default {
    data() {
        return {
            title: 'Water Invoices',
            tableName: 'Invoices'
        }
    },
    components: {
        BotoesExportacao,
        TabelaFaturas,
        Footer
    }
}
</script>

<style scoped>
.logo img{
    width: 20%;
    height: 20%;
}

.logo p{
    color: #12130F;
    font-size: 50px;
    font-weight: bold;
    text-align: center;
}

.box{
    padding: 1% 1%;
    border: 5px solid #12130F;
    border-radius: 10px 10px 10px 10px; 
    background-color: #42C2E2;
    box-shadow: 0 0 50px rgba(0, 0, 0, 0.1);
}

.box h2{
    color: #12130F;
    font-size: 25px;
    font-weight: bold;
}
</style>
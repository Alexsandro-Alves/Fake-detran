<template>
    <div>
        <ul v-for="dados in dadosVeiculo" :key="dados.PLACA">
        <li>PLACA: {{dados.PLACA}}</li>
        <li>LOCALIDADE: {{dados.LOCALIDADE}}</li>
        <li>DATAHORA: {{dados.DADOS_INFRACAO.DATAHORA}}</li>
        <li>TIPO: {{dados.DADOS_INFRACAO.TIPO}}</li>
        <li v-if="dados.DADOS_INFRACAO.VALOR">VALOR: {{dados.DADOS_INFRACAO.VALOR}}</li>
        <li v-if="dados.DADOS_INFRACAO.VEL_MAXIMA">VEL_MAXIMA: {{dados.DADOS_INFRACAO.VEL_MAXIMA}}</li>
        </ul>
    </div>
</template>


<script>
export default {
    computed: {
        dadosVeiculo() {
            return this.$store.state.dadosVeiculo
        }
    }
}
</script>

<style>

</style>
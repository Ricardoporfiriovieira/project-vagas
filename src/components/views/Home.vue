<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <FavoritarVagas></FavoritarVagas>
    <div class="container py-4">
        <div class="row">
            <div class="col">
                <PesquisarVagas></PesquisarVagas>
            </div>
        </div>

        <div class="row mt-5" v-for="(vaga, index) in vagas" :key="index">
            <div class="col-xs-1-12">
                <Vaga
                :titulo="vaga.titulo"
                :descricao="vaga.descricao"
                :salario="vaga.salario"
                :modalidade="vaga.modalidade"
                :tipo="vaga.tipo"
                :publicacao="vaga.publicacao"
                ></Vaga>
            </div>
        </div>

    
        <div class="row mt-5">
            <div class="col-12 col-sm-6 col-md-4 col-lg-4 mb-4">
                <CardIndicador titulo="Vagas disponíveis" :indicador="numberOfVagas"></CardIndicador>
            </div>

            <div class="col-12 col-sm-6 col-md-4 col-lg-4 mb-4">
                <CardIndicador titulo="Profissionais disponíveis" indicador="125"></CardIndicador>
            </div>

            <div class="col-12 col-sm-6 col-md-4 col-lg-4 mb-4">
                <CardIndicador titulo="Usuarios cadastrados" indicador="200"></CardIndicador>
            </div>
        </div>

    </div>
</template>

<script>

    import PesquisarVagas from '@/components/comuns/PesquisarVagas.vue'
    import CardIndicador from '@/components/comuns/CardIndicador.vue'
    import Vaga from '@/components/comuns/Vaga.vue'
    import FavoritarVagas from '@/components/comuns/FavoritarVagas.vue'

    export default {
        components: {
            PesquisarVagas,
            CardIndicador,
            Vaga,
            FavoritarVagas,
        },

        computed:{
            numberOfVagas(){
                return localStorage.length
            },

            vagas(){
                let vagas = []
                let i;

                for(i = 1; i <= localStorage.length; i++){
                    vagas.push(JSON.parse(localStorage.getItem(i.toString())))
                }

                return vagas
            }
        },

        data: () => ({
            
        })
    }
</script>

<style>

</style>
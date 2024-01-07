<template>
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
            <div class="col-4">
                <CardIndicador titulo="Vagas disponíveis" indicador="15"></CardIndicador>
            </div>

            <div class="col-4">
                <CardIndicador titulo="Profissionais disponíveis" indicador="125"></CardIndicador>
            </div>

            <div class="col-4">
                <CardIndicador titulo="Usuarios cadastrados" indicador="200"></CardIndicador>
            </div>
        </div>
        
    </div>
</template>

<script>

    import PesquisarVagas from '@/components/comuns/PesquisarVagas.vue'
    import CardIndicador from '@/components/comuns/CardIndicador.vue'
    import Vaga from '@/components/comuns/Vaga.vue'

    export default {
        components: {
            PesquisarVagas,
            CardIndicador,
            Vaga,
        },
        data: () => ({
            vagas: [
                {
                    titulo: 'Analista Programador PHP Pleno',
                    descricao: 'Profissional com conhecimentos em PHP, Laravel e MySQL. Necessário 3 anos de experiências. Atuará na manutenção de sistemas legados da empresa.',
                    salario: 6000,
                    modalidade: 'Home Office',
                    tipo: 'PJ',
                    publicacao: '2021-10-10'
                },
                {
                    titulo: 'Programador JavaScript Angular',
                    descricao: 'Profissional com conhecimentos avançados em JavaScript e Angular.',
                    salario: 5000,
                    modalidade: 'Presencial',
                    tipo: 'CLT',
                    publicacao: '2021-10-07'
                },
                {
                    titulo: 'Programador JavaScript Vue',
                    descricao: 'Profissional com conhecimentos avançados em JavaScript e Vue.',
                    salario: 5000,
                    modalidade: 'Home Office',
                    tipo: 'CLT',
                    publicacao: '2021-10-06'
                },
                {
                    titulo: 'Analista de Banco de Dados Sênior',
                    descricao: 'Domínio dos bancos de dados SQL Server, Oracle, Postgre e MySQL',
                    salario: 9000,
                    modalidade: 'Presencial',
                    tipo: 'PJ',
                    publicacao: '2021-10-06'
                },
                {
                    titulo: 'Programador Web Júnior',
                    descricao: 'Conhecimentos básicos em HTML, CSS, JavaScript, Bootstrap, PHP e MySQL',
                    salario: 3000,
                    modalidade: 'Presencial',
                    tipo: 'CLT',
                    publicacao: '2021-10-05'
                }
            ]
        })
    }
</script>

<style>

</style>
<template>
    <div class="container py-4">

        <div class="form-group mt-5">
        <label for="">Titulo: Apresente sua vaga para milhares de Profissionais de Graça</label>
        <input type="text"
            class="form-control" name="" id="" aria-describedby="helpId" placeholder="" v-model="titulo">
        <small id="helpId" class="form-text text-muted">Exemplo: Programador Python</small>
        </div>

        <div class="form-group mt-5">
          <label for="">Descrição</label>
          <textarea class="form-control" name="" id="" rows="3" v-model="descricao"></textarea>
          <small id="helpId" class="form-text text-muted">Informe os detalhes da vaga</small>
        </div>

        <div class="row mt-5">
            <div class="col-12 col-sm-6 col-md-4 col-lg-4">
                <div class="form-group">
                <label for="">Salario</label>
                <input type="text"
                    class="form-control" name="" id="" aria-describedby="helpId" placeholder="" v-model="salario">
                <small id="helpId" class="form-text text-muted">Informe o Salário</small>
                </div>
            </div>

            <div class="col-12 col-sm-6 col-md-4 col-lg-4">
                <div class="form-group">
                <label for="">Modalidade</label>
                <select class="form-control form-control-sm" name="" id="" v-model="modalidade">
                    <option value="" disabled>Selecione</option>
                    <option>Home Office</option>
                    <option>Presencial</option>
                    <option>Hibrido</option>
                </select>
                <small id="helpId" class="form-text text-muted">Informe onde as atividades serão realizadas</small>
                </div>
            </div>

            <div class="col-12 col-sm-6 col-md-4 col-lg-4">
                <div class="form-group">
                <label for="">Tipo</label>
                <select class="form-control form-control-sm" name="" id="" v-model="tipo">
                    <option value="" disabled>Selecione</option>
                    <option>CLT</option>
                    <option>Pessoa Juridica (PJ)</option>
                    <option>Hibrido</option>
                </select>
                <small id="helpId" class="form-text text-muted">Informe o tipo de contratação</small>
                </div>
            </div>
        </div>

        <button type="button" name="" id="" class="mt-3 btn btn-dark btn-lg btn-block" @click="save()" >Cadastrar</button>

    </div>
</template>

<script>

    export default {
        data: () => ({
            titulo: '',
            descricao: '',
            salario: '',
            modalidade: '',
            tipo: '',
            id: 1
        }),
        methods:{
            save() {

                let vagas = JSON.parse(localStorage.getItem('vagas'))

                console.log(localStorage.length) 

                

                if(!vagas) vagas = {}

                let vaga = {
                    id: localStorage.length + 1,
                    titulo: this.titulo,
                    descricao: this.descricao,
                    salario: this.salario,
                    modalidade: this.modalidade,
                    tipo: this.tipo
                }

                localStorage.setItem(localStorage.length + 1, JSON.stringify(vaga))
            }
        }
    }

</script>

<style>

</style>
<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">Vagas</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
            <a class="nav-link active" href="#" @click="navegarHome()">Home</a>
            </li>
            <li class="nav-item">
            <a class="nav-link" href="#" @click="navegarPublicarVaga()">Publicar Vaga</a>
            </li>
        </ul>
        </div>
    </div>
    </nav>
</template>

<script>
    export default {
        methods: {
            navegarPublicarVaga() {
                this.$emit(
                'EventPublicarVaga',
                {screen: 'PublicarVagas'}
                )
            },
            navegarHome() {
                this.$emit(
                'EventHome',
                {screen: 'Home'}
                )  
            }
        },
    }

</script>

<style>

</style>
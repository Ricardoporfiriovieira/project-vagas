<!-- eslint-disable vue/multi-word-component-names -->
<!-- eslint-disable vue/no-unused-components -->
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
                        <a class="nav-link active" href="#" @click="renderPageHome()">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" @click="renderPagePublicarVaga()">Publicar Vaga</a>
                    </li>
                    <!-- <li>
                        <FavoritarVagas></FavoritarVagas>
                    </li> -->
                </ul>

            </div>
        </div>
        
    </nav>
    
</template>

<script>

    import FavoritarVagas from "@/components/comuns/FavoritarVagas.vue"

    export default {
        methods: {
            renderPageHome() {
                this.$emit(
                'RenderHome',
                {ComponentToRender: 'Home'}
                )  
            },
            renderPagePublicarVaga() {
                this.$emit(
                'RenderPublicarVaga',
                {ComponentToRender: 'PublicarVaga'}
                )
            }
        },
        components: {
            FavoritarVagas,
        }
    }

</script>

<style>

</style>
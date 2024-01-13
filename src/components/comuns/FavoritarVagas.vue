<template>
    <div class="FavoritarVagas">
        <button
            class="btn btn-primary"
            type="button"
            data-bs-toggle="offcanvas"
            data-bs-target="#Id1"
            aria-controls="Id1"
        >
            Favoritar Vagas
        </button>
        
        <div
            class="offcanvas offcanvas-end"
            data-bs-scroll="true"
            tabindex="-1"
            id="Id1"
            aria-labelledby="Enable both scrolling & backdrop"
        >
            <div class="offcanvas-header d-flex justify-content-center">
                
                <h5 class="text-center offcanvas-title mx-5" id="Enable both scrolling & backdrop">
                    Vagas Favoritadas
                </h5>
                <button
                    type="button"
                    class="btn-close mr-5"
                    data-bs-dismiss="offcanvas"
                    aria-label="Close"
                ></button>
            </div>
            <div class="offcanvas-body">
                <p>
                    Nada aqui por enquanto
                </p>
            </div>
        </div>
    </div>
</template>

<script>

</script>

<style scoped>

.FavoritarVagas {
    position: absolute;
    top: 10px;
    right: 10px;
}

</style>
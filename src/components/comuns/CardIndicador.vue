<template>
    <div>
        <div class="h-100 p-5 bg-dark text-white border rounded-3">
            <p> {{ titulo }} </p>
            <h2> {{ indicador }} </h2>
        </div>
    </div>
</template>

<script>

    export default {
        props: ['titulo', 'indicador']
    }

</script>

<style>

</style>
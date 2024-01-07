<template>
    <div class="card">
        <div class="card-header">
            {{ titulo  }}
        </div>
        <div class="card-body">
            <h4 class="card-title">{{ titulo  }}</h4>
            <p class="card-text">{{ descricao  }}</p>
        </div>
        <div class="card-footer text-muted">
            {{ salario }} |
            {{ modalidade  }} |
            {{  tipo  }} |
            {{  publicacao  }} 
        </div>
    </div>
</template>

<script>
    export default {
        props: ['titulo', 'descricao', 'salario', 'modalidade', 'tipo', 'publicacao']
    }

</script>

<style>

</style>
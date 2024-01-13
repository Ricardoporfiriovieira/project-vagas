<!-- eslint-disable vue/no-parsing-error -->
<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="card">
        <div class="card-header position-relative">
            <div>{{ titulo }}</div>

            <div class="form-check form-switch position-absolute top-50 end-0 translate-middle">
                <label class="form-check-label">
                    <input type="checkbox" class="form-check-input" name="" id="" value="checkedValue">
                        Favoritar
                </label>
            </div>
            
        </div>
        <div class="card-body">
            <h4 class="card-title">{{ titulo  }}</h4>
            <p class="card-text">{{ descricao  }}</p>
        </div>
        <div class="card-footer text-muted">
            {{ salario }} |
            {{ modalidade  }} |
            {{  tipo  }} 
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
<template>
    <div class="card">
        <div class="card-header bg-dark text-white">{{ titulo }}</div>
        <div class="card-body">
            <p>{{ descricao }}</p>
        </div>
        <div class="card-footer">
            <small class="text-muted">Salário: R$ {{ salario }}| Modalidade: {{ modalidade }} | Tipo: {{ tipo }} |
                Publicação: {{ getPublicacao }}
            </small>
        </div>
    </div>
</template> 

<script>
export default {
    props: ['titulo', 'descricao', 'salario', 'modalidade', 'tipo', 'publicacao'],
    computed: {
        getPublicacao() {
            let dataPublicacao = new Date(this.publicacao)
            return dataPublicacao.toLocaleDateString('pt-BR')
        }
    }
}
</script>
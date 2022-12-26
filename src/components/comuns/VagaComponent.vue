<template>
    <div class="card">
        <div class="card-header bg-dark text-white">
            <div class="row">
                <div class="col d-flex justify-content-between">
                    <div>
                        {{ titulo }}
                    </div>
                    <div>
                        <div class="form-check form-switch">
                            <input class="form-check-input" type="checkbox">
                            <label class="form-check-label">Favoritar</label>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>
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
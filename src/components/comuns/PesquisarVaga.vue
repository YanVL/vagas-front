<script>
export default {
    data: () => ({
        titulo: ''
    }),
    methods: {
        pesquisarVaga() {
            this.emitter.emit('filtrarVagas', { titulo: this.titulo })
        }
    }
}
</script>

<template>
    <div class="h-100 p-5 bg-light border hounded-3">

        <h2>Pesquisar Vagas</h2>
        <div class="row">
            <div class="col">
                <div class="mb-3">
                    <label class="form-label">Título da vaga</label>
                    <input type="text" class="form-control" placeholder="Pesquise por palavras-chave" v-model="titulo">
                    <small id="helpId" class="text-muted">Informe palavras relacionadas com as vagas que você
                        procura</small>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <button class="btn btn-outline-dark mt-2" type="button" @click="pesquisarVaga()">Buscar</button>
            </div>
        </div>
    </div>
</template>

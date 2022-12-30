<script>
import Alerta from '@/components/comuns/AlertaComponent.vue';
import Conteudo from '@/components/layouts/ConteudoComponent.vue'
import VagasFavoritas from './components/comuns/VagasFavoritas.vue';
import Topo from '@/components/layouts/TopoComponent.vue'

export default {
  data: () => ({
    visibilidade: true,
    componente: 'HomeComponent',
    exibirAlerta: false,
    alerta: { titulo: '', descricao: '', tipo: '' }
  }),
  components: {
    Alerta,
    Conteudo,
    Topo,
    VagasFavoritas,
  },
  mounted() {
    this.emitter.on('alerta', (a) => {
      this.alerta = a
      this.exibirAlerta = true
      setTimeout(() => this.exibirAlerta = false, 10000);
    })
  }
}
</script>

<template>
  <div>
    <VagasFavoritas></VagasFavoritas>
    <Topo @navegar="componente = $event" />
    <Alerta v-if="exibirAlerta" :tipo="alerta.tipo">
      <template v-slot:titulo>
        <h5>{{ alerta.titulo }}</h5>
      </template>
      <p>{{ alerta.descricao }}</p>
    </Alerta>
    <Conteudo v-if="visibilidade" :conteudo="componente"></Conteudo>
  </div>
</template>

<style>

</style>

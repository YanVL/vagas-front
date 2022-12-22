<script>
import Conteudo from '@/components/layouts/ConteudoComponent.vue'
import Topo from '@/components/layouts/TopoComponent.vue'

export default {
  data: () => ({
    visibilidade: true,
    componente: 'HomeComponent'
  }),
  components: {
    Conteudo,
    Topo
  }
}
</script>

<template>
  <div>
    <Topo @navegar="componente = $event" />
    <Conteudo v-if="visibilidade" :conteudo="componente"></Conteudo>
  </div>
</template>

<style>

</style>

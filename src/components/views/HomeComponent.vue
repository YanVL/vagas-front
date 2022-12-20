<script>
import PesquisarVaga from '@/components/comuns/PesquisarVaga.vue'
import IndicadorComponent from '@/components/comuns/IndicadorComponent.vue'

export default {
  components: {
    PesquisarVaga,
    IndicadorComponent
  },
  data: () => ({
    usuariosOnline: 0
  }),
  methods: {
    getUsuariosOnline() {
      this.usuariosOnline = Math.floor(Math.random() * 101)
    }
  },
  created() {
    setInterval(this.getUsuariosOnline, 1000);
  }
}
</script>

<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <PesquisarVaga></PesquisarVaga>
      </div>
    </div>

    <div class="row mt-5">
      <div class="col-4">
        <IndicadorComponent titulo="Vagas Abertas" indicador="100" bg="bg-dark" color="text-white"></IndicadorComponent>
      </div>

      <div class="col-4">
        <IndicadorComponent titulo="Profissionais cadastrados" indicador="225" bg="bg-dark" color="text-white"></IndicadorComponent>
      </div>

      <div class="col-4">
        <IndicadorComponent titulo="Visitantes online" :indicador="usuariosOnline" bg="bg-light" color="text-dark"></IndicadorComponent>
      </div>
    </div>

  </div>
</template>

<style>

</style>

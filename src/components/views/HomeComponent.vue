<script>
import PesquisarVaga from '@/components/comuns/PesquisarVaga.vue'
import IndicadorComponent from '@/components/comuns/IndicadorComponent.vue'
import VagaComponent from '@/components/comuns/VagaComponent.vue'

export default {
  components: {
    PesquisarVaga,
    IndicadorComponent,
    VagaComponent,
  },
  data: () => ({
    usuariosOnline: 0,
    vagas: []
  }),
  methods: {
    getUsuariosOnline() {
      this.usuariosOnline = Math.floor(Math.random() * 101)
    }
  },
  created() {
    setInterval(this.getUsuariosOnline, 1000);
  },
  mounted() {
    this.vagas = JSON.parse(localStorage.getItem('vagas'))
    this.emitter.on('filtrarVagas', vaga => {
      const vagas = JSON.parse(localStorage.getItem('vagas'))
      this.vagas = vagas.filter(reg => reg.titulo.toLowerCase().includes(vaga.titulo.toLowerCase()))
    })
  },

}
</script>

<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <PesquisarVaga></PesquisarVaga>
      </div>
    </div>

    <div class="row mt-5" v-for="(vaga, index) in vagas" :key="index">
      <div class="col">
        <VagaComponent v-bind="vaga"></VagaComponent>
      </div>
    </div>

    <div class="row mt-5">
      <div class="col-4">
        <IndicadorComponent titulo="Vagas Abertas" indicador="100" bg="bg-dark" color="text-white"></IndicadorComponent>
      </div>

      <div class="col-4">
        <IndicadorComponent titulo="Profissionais cadastrados" indicador="225" bg="bg-dark" color="text-white">
        </IndicadorComponent>
      </div>

      <div class="col-4">
        <IndicadorComponent titulo="Visitantes online" :indicador="usuariosOnline" bg="bg-light" color="text-dark">
        </IndicadorComponent>
      </div>
    </div>

  </div>
</template>

<style>

</style>

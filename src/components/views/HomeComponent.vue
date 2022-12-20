<script>
import PesquisarVaga from '@/components/comuns/PesquisarVaga.vue'
import IndicadorComponent from '@/components/comuns/IndicadorComponent.vue'

export default {
  components: {
    PesquisarVaga,
    IndicadorComponent
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
        <IndicadorComponent></IndicadorComponent>
      </div>

      <div class="col-4">
        <IndicadorComponent></IndicadorComponent>
      </div>

      <div class="col-4">
        <IndicadorComponent></IndicadorComponent>
      </div>

    </div>

  </div>
</template>

<style>

</style>

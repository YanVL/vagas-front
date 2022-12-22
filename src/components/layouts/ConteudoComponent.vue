<script>
import HomeComponent from '@/components/views/HomeComponent.vue'
import PublicarVaga from '@/components/views/PublicarVaga.vue'

export default {
  props: {
    conteudo: {
      type: String,
      required: true
    }
  },
  components: {
    HomeComponent,
    PublicarVaga
  }
}
</script>

<template>
  <div>
    <keep-alive>
      <component :is="conteudo" />
    </keep-alive>
  </div>
</template>

<style>

</style>

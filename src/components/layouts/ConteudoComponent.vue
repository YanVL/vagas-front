<script>
import HomeComponent from '@/components/views/HomeComponent.vue'
import PublicarVaga from '@/components/views/PublicarVaga.vue'

export default {
    components: {
      HomeComponent,
      PublicarVaga
    },
    data: () => ({
      teste: 'O componente foi criado',
      titulo: 'Componente Conteudo',
      conteudo: 'home-component'
    }),
    methods: {
      atualizarComponente() {
        this.titulo += '*'
      }
    },
  }
</script>

<template>
  <div>

    <button @click="conteudo = 'home-component'">Home</button>
    <button @click=" conteudo = 'publicar-vaga'">Publicar vaga</button>    

    <component :is="conteudo"></component>

  </div>
</template>

<style>

</style>

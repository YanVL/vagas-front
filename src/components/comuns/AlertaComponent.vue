<script>
export default {
  props: { tipo: String },
  computed: {
    estiloAlerta() {
      switch(this.tipo) {
        case 'erro': return 'alert alert-danger'
        case 'sucesso': return 'alert alert-success'
        default: return 'alert alert-success'
      }
    }
  }
}

</script>

<template>
  <div :class="estiloAlerta" role="alert">
    <slot name="titulo">
      <h3>Titulo da mensagem do Feedback</h3>
    </slot>
    <hr>
    <slot>
      <p>Mensagem de Feedback</p>
    </slot>
  </div>
</template>
<script>

</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h4>Apresente a sua vaga para milhares de profissionais de graça</h4>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Título da vaga</label>
        <input type="text" class="form-control">
        <div class="form-text">Por exemplo: Programador JavaScript e VueJs.</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Descrição</label>
        <textarea type="text" class="form-control"></textarea>
        <div class="form-text">Informe os detalhes da vaga.</div>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Salário</label>
        <input type="number" class="form-control">
        <div class="form-text">Informe o Salário</div>
      </div>
    </div>

    <div class="col">
      <label class="form-label">Modalidade</label>
      <select class="form-select">
        <option value="1">Home Office</option>
        <option value="2">Presencial</option>
      </select>
      <div class="form-text">Informe a modalidade de trabalho</div>
    </div>

    <div class="col">
      <label class="form-label">Tipo</label>
      <select class="form-select">
        <option value="1">CLT</option>
        <option value="2">PJ</option>
      </select>
      <div class="form-text">Informe tipo de contratação</div>
    </div>

    <div class="row">
      <div class="col">
        <button class="btn btn-primary">Cadastrar</button>
      </div>
    </div>

  </div>
</template>

<style>

</style>

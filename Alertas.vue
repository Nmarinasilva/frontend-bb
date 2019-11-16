<template>
  <div class="row justify-content-center">
    <div class="col-lg-5 col-md-7">
      <div class="card bg-secondary shadow border-0">
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <big>Gerenciador de Alertas</big>
          </div>
          <form role="form">
            <base-input
              class="input-group-alternative mb-3"
              placeholder="Item"
              addon-left-icon="ni ni-hat-3"
              v-model="model.item"
            ></base-input>

            <base-input
              class="input-group-alternative mb-3"
              placeholder="Quantidade Miníma"
              addon-left-icon="ni ni-hat-3"
              v-model="model.quantidademin"
            ></base-input>

            <base-input
              class="input-group-alternative mb-3"
              placeholder="Tipo de Alerta"
              addon-left-icon="ni ni-hat-3"
              v-model="model.tipoalerta"
            ></base-input>

            <base-input
              class="input-group-alternative mb-3"
              placeholder="PIN"
              addon-left-icon="ni ni-hat-3"
              v-model="model.pin"
            ></base-input>
            <hr />
              <div class="text-center">
              <base-button type="primary" class="my-4">Definir</base-button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "alertas",
  data() {
    return {
      model: {
        item: "",
        quantidade minima: "",
        tipo de alerta: "",
        situação: "",
        PIN: "",
        atualizar: ""
      }
    };
  }
};
</script>
<style>
</style>

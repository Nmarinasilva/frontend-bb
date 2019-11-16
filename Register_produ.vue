<template>
  <div class="row justify-content-center">
    <div class="col-lg-5 col-md-7">
      <div class="card bg-secondary shadow border-0">
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <big>Adicionar Item</big>
          </div>
          <form role="form">
            <base-input
              class="input-group-alternative mb-3"
              placeholder="Item"
              addon-left-icon="ni ni-zoom-split-in"
              v-model="model.item"
            ></base-input>

            <base-input
              class="input-group-alternative mb-3"
                placeholder="Tipo de Item"
              addon-left-icon="ni ni-hat-3"
              v-model="model.tipo_item"
            ></base-input>

            <base-input
              class="input-group-alternative mb-3"
              placeholder="Categoria"
              addon-left-icon="ni ni-hat-3"
              v-model="model.categoria"
            ></base-input>

            <base-input
              class="input-group-alternative mb-3"
              placeholder="Unidades"
              addon-left-icon="ni ni-hat-3"
              v-model="model.uni"
            ></base-input>
            <hr />
            <base-input
              class="input-group-alternative mb-3"
              placeholder="Fornecedor"
              addon-left-icon="ni ni-email-83"
              v-model="model.forne"
            ></base-input>

            <base-input
              class="input-group-alternative"
              placeholder="Lote"
              addon-left-icon="ni ni-lock-circle-open"
              v-model="model.lote"
            ></base-input>
            <div class="text-center">
              <base-button type="primary" class="my-4">Adicionar Item</base-button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "register_produ",
  data() {
    return {
      model: {
       Item: "",
        Tipo de Item: "",
        Categoria: "",
        Unidades: "",
        Fornecedor: "",
        Lote: "",
        Preço de Compra: "",
        Data de Validade: "",
        Quantidade: "",
        PIN: ""
      }
    };
  }
};
</script>
<style>
</style>

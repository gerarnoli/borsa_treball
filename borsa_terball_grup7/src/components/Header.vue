<template>
  <v-footer padless>
    <v-col
      class="text-left indigo float-left"
      cols="12"
    >
      <v-btn
        color="primary"
        rounded        
      >Iniciar Sessió</v-btn>
      <v-divider
        class="ma-4"
        vertical
        style="display: inline"
      ></v-divider>
      <b-button v-b-modal.modal-3 class="admin" variant="primary">Registro</b-button>
      <Register/>




      <b-button v-b-modal.modal-1 class="empresa" variant="primary">Ets empresa?</b-button>
    </v-col>  
  </v-footer>
</template>

<script>

import Register from './Register';

export default {
    name: 'Header',
    components: {
        Register
    },
    datos: () => ({
    //
  }),
};
</script>

<style scoped>
.empresa {
  float: right;
}



</style>

<template>
  <v-header padless>
    <v-col class="text-left indigo float-left" cols="12">
      <v-btn color="primary" rounded>Iniciar Sessió</v-btn>
      <v-divider class="ma-4" vertical style="display: inline"></v-divider>
      <b-button href="https://localhost:8000/oferta/new" class="empresa" variant="primary">Ets empresa?</b-button>
  <b-button v-b-modal.modal-3 class="admin" variant="primary">Registro</b-button>
      <Register/>

    </v-col>  
  </v-header>
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
  color: white;
}



</style>

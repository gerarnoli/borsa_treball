<template>
  <v-header padless>
    <v-col class="text-left indigo float-left" cols="12">
      <v-btn color="primary" rounded>Iniciar Sessió</v-btn>
      <v-divider class="ma-4" vertical style="display: inline"></v-divider>
      <v-btn color="primary" rounded>Registre</v-btn>
      <b-button href="https://localhost:8000/oferta/new" class="empresa" variant="primary">Ets empresa?</b-button>
    </v-col>  
  </v-header>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup() {
  }
})
</script>

<style scoped>
.empresa {
  float: right;
  color: white;
}
</style>

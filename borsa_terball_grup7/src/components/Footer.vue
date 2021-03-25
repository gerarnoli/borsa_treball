<template>
  <v-footer padless absolute>
    <v-col class="text-center indigo lighten-2" cols="12">
      <b-button v-b-modal.modal-2 class="admin" variant="primary">Admin</b-button>
      <strong>GRUP 7</strong> — {{ new Date().getFullYear() }}
    </v-col>
  </v-footer>
</template>

<style scoped>
.admin {
  float: left;
  color: white;
}
</style>
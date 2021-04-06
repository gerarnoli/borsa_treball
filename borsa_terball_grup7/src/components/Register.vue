<template>
<div>
  <v-footer padless>
   

    <b-modal id="modal-3" title="Register">
      <b-form @submit="onSubmit" @reset="onReset" v-if="mostrar">
        <b-form-group id="input-group-3" label="Usuari" label-for="input-3">
          <b-form-input
            id="input-3"
            v-model="form.usuari"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-3" label="Contrasenya" label-for="input-3">
          <b-form-input
            id="input-4"
            v-model="form.contrasenya"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>

        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
      </b-form>
    </b-modal>

</v-footer>
</div>
</template>

<script>

export default {
    datos() {
      return {
        form: {
          usuari: '',
          contrasenya: '',
          checked: []
        },
        mostrar: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.usuari = ''
        this.form.contrasenya = ''
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.mostrar = false
        this.$nextTick(() => {
          this.mostrar = true
        })
      }
    }
  }
</script>

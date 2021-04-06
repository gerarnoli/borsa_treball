<template>
  <div>
    <b-modal id="modal-2" title="Admin">
      <b-form @submit="onSubmit" @reset="onReset" v-if="show">
        <b-form-group id="input-group-2" label="Usuari" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.usuari"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Contrasenya" label-for="input-2">
          <b-form-input
            id="input-3"
            v-model="form.contrasenya"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>
        <b-button :disabled='isDisabled' type="submit" href="http://localhost:8000/oferta/" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
      </b-form>
    </b-modal>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          usuari: '',
          contrasenya: '',
          checked: []
        },
        show: true
      }
    },
    computed: {
      isDisabled: function () {
        if (this.form.usuari != "ausias" || this.form.contrasenya != "ausias") {
          return true;
        }
        return false;
      }
    },
    methods: {
      onSubmit() {
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
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script> 
<template>
  <div class="empresa">
    <b-modal id="modal-1" title="Oferta">
      <b-form @submit="onSubmit" @reset="onReset" v-if="show">
        <b-form-group
        id="input-group-1"
        label="Títol"
        label-for="input-1"
        description=""
        >
          <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Descripció" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.descripcio"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-3" label="Nom de l'empresa" label-for="input-3">
          <b-form-input
            id="input-3"
            v-model="form.name"
            placeholder=""
            required
          ></b-form-input>
        </b-form-group>

        <b-button type="submit" variant="primary">Submit</b-button>
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
          email: '',
          descripcio: '',
          name: '',
          checked: []
        },
        show: true
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
        this.form.email = ''
        this.form.descripcio = ''
        this.form.name = ''
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!--
<style scoped>
.empresa {
    margin-left: 35%;
    margin-right: 35%;
    margin-top: 10%;
    margin-bottom: 10%;
}
</style>
-->
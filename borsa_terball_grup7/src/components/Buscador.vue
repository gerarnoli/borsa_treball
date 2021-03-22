<template>
<div>
    <h1>prova Buscador</h1>
    <b-button @click="pedirDatos" variant="primary">Cerrar</b-button>
</div>       
</template>


<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';

Vue.use(VueAxios, axios);

export default{
      data() {
          return{
              resultados: []
          }
        
    },
    methods: {
        pedirDatos() {
            axios.get(`http://labs.iam.cat/~a16pednieper/treball_g7/api_treball.php/records/oferta`).then((response) => {this.resultados = response.data.records; console.log(response) })
        }
    }
}
</script>

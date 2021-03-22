<template>
<div>
    <h1>prova Buscador</h1>
    <b-button @click="pedirDatos" variant="primary">Cerrar</b-button>
    <!-- <b-row>
        <b-card-group deck>
        <fichaPelicula v-for="oferta in resultado"
            :key=pelicula.imdbID
            :infoPelicula=pelicula>
        </fichaPelicula>
        </b-card-group>
    </b-row> -->
    <Oferta/>
</div>
</template>

<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';
import Oferta from './Oferta.vue';

Vue.use(VueAxios, axios);

export default{
    name: 'Buscador',
    components: {
        Oferta
    },
    methods: {
        pedirDatos() {
            this.axios.get(`http://labs.iam.cat/~a16pednieper/treball_g7/api_treball.php/records/oferta`).then((response) => {this.resultados = response.data.records; console.log(response) })
        }
    },
    data() {
        return{
            resultado: []
        }
    },
}
</script>

<template>
<div>
    <h1>prova Buscador</h1>
    <b-button @click="pedirDatos" variant="primary">Pedir datos</b-button>
    <b-row>
        <b-card-group deck>
        <Oferta v-for="oferta in resultado"
            :key=oferta.id
            :infoOferta=oferta>
        </Oferta>
        </b-card-group>
    </b-row>
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
            this.axios.get(`http://labs.iam.cat/~a16pednieper/treball_g7/api_treball.php/records/oferta`).then((response) => {
                this.resultado = response.data.records;
                console.log(this.resultado);
            })
        }
    },
    data() {
        return{
            resultado: []
        }
    },
}
</script>

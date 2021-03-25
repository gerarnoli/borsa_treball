<template>
<div>
    <b-button @click="pedirDatos" variant="success" class="ofertes">Mostrar ofertes</b-button>
    <b-row>
        <b-card-group deck>
            <Oferta v-for="oferta in resultado"
                :key=oferta.id
                :infoOferta=oferta>
            </Oferta>
        </b-card-group>
        <!--class="col-md-2"-->
    </b-row>
</div>
</template>

<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';
import Oferta from './Oferta.vue';

Vue.use(VueAxios, axios);

export default {
    name: 'Buscador',
    components: {
        Oferta
    },
    data() {
        return{
            resultado: []
        }
    },
    methods: {
        pedirDatos: function () {
            this.axios.get(`http://labs.iam.cat/~a16pednieper/treball_g7/api_treball.php/records/oferta?filter=estat,gt,0`).then((response) => {
                console.log(response.data.records);
                this.resultado = response.data.records;
            })
        }
    }
}
</script>

<style>
.ofertes {
    margin: 10px;
    margin-bottom: 30px;
}
</style>

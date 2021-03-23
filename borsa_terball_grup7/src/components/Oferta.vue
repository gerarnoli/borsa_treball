<template>
    <div>
    <b-card
        :title=oferta.titol
        img-src="https://picsum.photos/600/300/?image=25"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
    >
        <b-card-text>
            {{this.infoOferta.descripcio}}
        </b-card-text>
        <b-button variant="primary">Go somewhere</b-button>
    </b-card>
    </div>
</template>

<script>
export default {
    name: 'Oferta',
    props: {
        infoOferta: Object
    },
    methods: {
        pedirDatos: function () {
            this.axios.get(`http://labs.iam.cat/~a16pednieper/treball_g7/api_treball.php/records/oferta`).then((response) => {
                console.log(response.data);
                this.resultados = response.data;
            })
        }
    }
}
</script>

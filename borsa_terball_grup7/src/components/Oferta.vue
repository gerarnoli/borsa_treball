<template>
    <h1>prova</h1>
</template>

<script>

export default{
    data() {
        
    },
    methods: {
        pedirDatos() {
            axios.get(`http://labs.iam.cat/~a16pednieper/treball_g7/api_treball.php/records/oferta`).then((response) => {this.detailedResults = response.data; console.log(response)})
        }
    }
}
</script>

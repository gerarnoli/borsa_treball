<template>
    <div>
    <b-card 
        v-bind:class="{ desactivada: infoOferta.estat==2 }"
        :title=infoOferta.titol        
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
    >
        <b-card-text>
            {{this.infoOferta.descripcio}}
        </b-card-text>
        <b-card-text>
            <em>{{this.infoOferta.ubicacio}}</em>
        </b-card-text>

    </b-card>
    </div>
</template>

<script>
export default {
    name: 'Oferta',
    props: {
        infoOferta: Object
    }
}
</script>

<style>
.desactivada{
    background-color: lightgrey !important;
}
</style>
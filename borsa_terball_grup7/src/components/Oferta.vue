<template>
    <div>
    <b-card
        :title=infoOferta.titol
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
        <b-button variant="primary">Més info</b-button>
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

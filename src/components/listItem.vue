<template>
    <b-col cols=6 sm=6 >
        <h3>Objeto: {{data.name}} - {{data.quantity}}</h3>
        <b-img fluid src="data.src" alt="data.alt" />
        <b-row align-v="center" class="justify-content-md-center">
            <b-button class="button" > + </b-button>
            <b-button class="button" > - </b-button>
        </b-row>
    </b-col>
</template>

<script>
export default {
    props:{
        data: {
            type: Array
        }
    },
    methods:{
        add(){

        },
        substract(){

        }
    }
}
</script>

<style>
    img{
        height:200px;
        width:auto;
    }
    .button{
        margin:5px;
    }
</style>
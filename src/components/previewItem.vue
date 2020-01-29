<template>
  <b-card
  >
    <h2>Objeto seleccionado: previewItem.name</h2>
    <h3>Cantidad: previewItem.quantity</h3>
    <b-img  src="previewItem.src" />
  </b-card>
</template>

<script>
export default {
    props:{
        previewItem:{
            type: Array
        }
    }
}
</script>

<style>
    b-card{
        width:200px;
    }
</style>
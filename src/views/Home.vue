<template>
  <div class="home">
    <b-container>
      <b-row class="justify-content-md-center">
        <b-col >
          <h2>Previsualización</h2>
          <PreviewItem :previewItem="previewItem" />
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <h2>Lista de items</h2>
        </b-col>
      </b-row>
      <b-row>
        <template v-for="(item, index) in items">
          <ListItem :data="item" :key="index" @object="itemClick"/>  
        </template>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import ListItem from '@/components/listItem.vue'
import PreviewItem from '@/components/previewItem.vue'

export default {
  name: 'home',
  components: {
    ListItem,
    PreviewItem
  },
  data(){
    return{
      items:[
        { quantity: 4, name:"Taza", src:"https://images.pexels.com/photos/1477851/pexels-photo-1477851.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260", alt:"taza" },
        { quantity: 5, name:"Lapicero", src:"https://images.pexels.com/photos/6440/magazines-desk-work-workspace.jpg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260", alt:"lapicero"},
        { quantity: 12, name:"Bolígrafo", src:"https://images.pexels.com/photos/372748/pexels-photo-372748.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260", alt:"bolígrafo"},
        { quantity: 3, name:"Notas Adhesivas", src:"https://images.pexels.com/photos/6183/office-notes-colorful-paper.jpg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260", atl:"notas"}
      ],
      previewItem:{}
    }
  },
  methods:{
  }
}
</script>

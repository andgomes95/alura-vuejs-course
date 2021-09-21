<template>
  <div>
    <h1>{{titulo}}</h1>
    <ul>
      <li v-for="(foto,index) of fotos" :key="index">
        <img :src="foto.url" :alt="foto.alt">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      titulo :'Alurapic',
      fotos:[]
    }
  },
  created() {
    this.$http.get('http://localhost:3000/v1/fotos')
      .then(res => res.json())
      .then(fotos => this.fotos = fotos, err => console.log(err));
  }
}
</script>

<style>

</style>

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
      fotos:[ {
        url: 'https://cdn.myanimelist.net/images/anime/1223/96541.jpg',
        alt: 'fma'
      },
      {
        url: 'https://cdn.myanimelist.net/images/anime/1548/116226.jpg',
        alt: 'slime'
      },
      {
        url: 'https://cdn.myanimelist.net/images/anime/1252/115539.jpg',
        alt: 'dragon'
      },
      ]
    }
  }
}
</script>

<style>

</style>

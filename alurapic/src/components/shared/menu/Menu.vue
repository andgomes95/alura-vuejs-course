<template>
  <nav>
    <ul>       
        <li v-for="rota in rotas" :key="rota.titulo">
          <router-link :to="rota.path ? rota.path : '/'">{{rota.titulo}}</router-link>
        </li>
    </ul>
  </nav>
</template>
<script>
export default {
  props: {
    rotas:{
      type: Array,
      required: true
    }
  }
}
</script>
<style scoped>
  .pagina-enter, .pagina-leave-active{
    opacity: 0;
  }
  .pagina-enter-active, .pagina-leave-active {
    transition: opacity .5s;
  }
</style>
<template>
  <div class="corpo">

    <meu-menu :rotas="routes"/>    
    <transition name="pagina">
      <router-view></router-view>
    </transition>

  </div>
</template>
<script>

import { routes }  from './routes';
import Menu from './components/shared/menu/Menu.vue'

export default {
  components: {
    'meu-menu': Menu
  },
  data() {

    return {

      routes
    }

  }

}
</script>
<style>

  .corpo {
    font-family: Helvetica, sans-serif;
    margin: 0 auto;
    width: 96%;
  }
</style>
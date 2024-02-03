<script>
import AppMain from './components/AppMain.vue'; 

export default{

  components: {AppMain},

  data(){
    return{

    }
    
  }
}
</script>

<template>
   <h1>App.vue</h1>
   <AppMain/>
</template>

<style lang="scss">
@use '../src/styles/general.scss' as *;
</style>
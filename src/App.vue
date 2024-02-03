<script>
import AppMain from './components/AppMain.vue'; 
import AppHeader from './components/AppHeader.vue'; 

export default{

  components: {AppMain,AppHeader},

  data(){
    return{
      
    }
    
  }
}
</script>

<template>
  <AppHeader />
  <h1>App.vue</h1>
  <router-view></router-view>
</template>

<style lang="scss">
@use '../src/styles/general.scss' as *;
</style>
<script>
import axios from 'axios';

export default{
  data(){
    return{
        baseUrl: 'http://127.0.0.1:8000',
        projects: []

    }
  },
  created() {
    axios.get(`${this.baseUrl}/api/projects`).then((resp) => {
        console.log(resp);
        this.projects = resp.data.results;
    })
  }
}

</script>

<template>
   <h1>main</h1>
</template>

<style lang="scss" scoped>

</style>

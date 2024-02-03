<script>
import axios from 'axios';
import ProjectCard from './ProjectCard.vue';

export default {

    components: {ProjectCard},

    data() {
        return {
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
    <h1>Projects:</h1>
    <div class="container">
        <div class="row row-cols-3 g-4">
            <div class="col" v-for="project in projects" :key="project.id">
               <ProjectCard :project="project"/>

            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>

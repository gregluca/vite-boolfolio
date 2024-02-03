<script>
import axios from 'axios';
import ProjectCard from './ProjectCard.vue';
import { store } from '../store';

export default {

    components: {ProjectCard},

    data() {
        return {
            store,
            projects: []

        }
    },
    created() {
        axios.get(`${this.store.baseUrl}/api/projects`).then((resp) => {
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

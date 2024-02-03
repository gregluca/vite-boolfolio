<script>
import { store } from '../store';
export default {
    props: {
        project: Object
    },
    data() {
        return {
            store
        }
    },
    computed: {
        truncateText() {
            if (this.project.description && this.project.description.length > 80) {
                return this.project.description.substring(0, 80) + "...";
            }
            return this.project.description;
        },
    },
}
</script>

<template>

    <div class="card h-100">
        <h5 class="card-header">{{ project.title }}</h5>
        <div class="card-body">
            <p class="mt-1">{{ truncateText }}</p>
        </div>
    </div>

</template>
<style lang="scss" scoped></style>
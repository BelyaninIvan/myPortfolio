<template>
  <ul class="projects__list">
    <ProjectsItem
      v-for="project in projectsList"
      :key="project.id"
      :projectsItem="project"
    >
    </ProjectsItem>
  </ul>
</template>
<script>
import ProjectsItem from '@/components/ProjectsItem.vue';
export default {
  name: 'ProjectsList',
  components: {
    ProjectsItem,
  },
  props: {
    projectsList: {
        type: Array,
    }
  }
}
</script>
<style scoped>
  .projects__list {
    margin: 0;
    padding: 0;
    list-style-type: none;

    display: grid;
    grid-template-columns: repeat(4, 250px);
    column-gap: 70px;
    row-gap: 40px;
  }
</style>
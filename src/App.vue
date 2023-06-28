<template>

  <pageProject v-if="project"></pageProject>
  <pageTask v-else></pageTask>
  <!-- <pageAbout></pageAbout> -->
</template>

<script>

import pageProject from './views/PageProject.vue';
import pageTask from './views/PageTask.vue';
// import pageAbout from './views/PageAbout.vue';

export default {
  components: {

    pageProject,
    pageTask,
    // pageAbout,
  },
  data() {
      return {
       project: true,
      //  project: false,
      }
    },

}
</script>

<style>
  @import './sass/style.scss';
  @import './sass/color.scss';
</style>
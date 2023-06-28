<template>
    <div class="wrapper">
        <header class="header">
            <navigation></navigation>
        </header>
        <main class="main">
            <taskItem v-if="dataLenght"></taskItem>
            <emptyTask v-else></emptyTask>
        </main>
    </div>
  </template>
  
  <script>
  
 import navigation from '../components/Navigation/NavigationVue.vue';
 import taskItem from '../components/TaskItems/TaskItem.vue';
 import emptyTask from '../components/TaskItems/EmptyTasks.vue';

  export default {
    components: {
        navigation,
        taskItem,
        emptyTask,
    },
    data() {
      return {
        dataLenght: true,
      }
    },
  }
  </script>

  <style lang="scss">

   .main{
      flex: 1 1 auto;
      width: 100%;
      min-height: 100%;
      overflow: hidden;
      display: flex;
      flex-direction: column;
   }
  </style>
  
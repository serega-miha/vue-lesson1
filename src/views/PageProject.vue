
<template>
      <div class="wrapper">
        <header class="header">
            <navigation></navigation>
        </header>
        <main class="main">
            <div class="main-search">
              <searchField
              :namePlaceholder="placeholder"
              ></searchField>
            </div>
            <div class="main-body">
              <projectItems v-if="dataLenght"></projectItems>
               <emptyTask v-else></emptyTask>
            </div>
            

        </main>
       
        
    </div>

  </template>
  
  <script>
 import navigation from '../components/Navigation/NavigationVue.vue';
 import projectItems from '../components/ProjectItems/ProjactItems.vue';
 import emptyTask from '../components/TaskItems/EmptyTasks.vue';
 import searchField from '../components/Input/InputOne.vue';
  export default {
    components: {
        navigation,
        projectItems,
        emptyTask,
        searchField,
    },

    data() {
      return {
        dataLenght: true,
        placeholder: 'какой то инпут'
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
  
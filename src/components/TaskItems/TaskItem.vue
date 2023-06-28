
 <template>
           <div class="project-items">
                <div class="project-items-container">
                    <taskItemOne
                    :task="task"
                    :key="index"
                    v-for="(task, index) in tasks"
                    ></taskItemOne>

                </div>
            </div>
 </template>
  <script>
  import '@/assets/icons/dots.svg';
  import taskItemOne from '../TaskItem/TaskItemOne.vue'
import {TasksDB} from '../../common/tasksItemDB.js'

 export default {
    components:{
        taskItemOne,
     },
   
     data() {
         return {
            tasks: TasksDB,

           
         }
     },
   
 }

 </script>

 <style lang="scss">
    
.project-items-container {
    margin: 20px;
  }
   
 </style>
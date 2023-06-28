
 <template>
        <div class="project-items">
            <div class="project-items-container">
                
                <projectItemOne
                    :proj="proj"
                    :key="index"
                    v-for="(proj, index) in projects"
                    ></projectItemOne>
                    
            </div>

        </div>
 </template>
 <script>

import projectItemOne from '../ProjectItem/ProjectItemOne.vue'
import {ProjectsDB} from '../../common/projectItemDB.js'

 export default {
    components:{
     
        projectItemOne,
    },
   
     data() {
         return {
            projects: ProjectsDB,

            
         }
     },
     
 }

 </script>

 <style lang="scss">

    @import '@/sass/color.scss';

.project-items-container {
    margin: 20px;
  }

 </style>
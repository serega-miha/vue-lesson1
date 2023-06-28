 <template>
   
   <div class="btn-addittionaly">
        <a class="button-addittionaly project-item__addittionaly" @click="menuVisible = !menuVisible">
                <iconSvg
                :className="classNameSvg"
                :nameSvg="nameSvg"
                ></iconSvg>
        </a>
        <div class="btn-update"  v-show="menuVisible">
                <ul class="update-menu__list">
                    <li class="update-menu__item">
                        <a href="#" class="update-menu__link">Редактировать</a>
                    </li>
                    <li class="update-menu__item">
                        <a href="#" class="update-menu__link update-menu__link-r">Удалить</a>
                    </li>
                </ul>

        </div>
    </div>
 
</template>
<script>
  import '@/assets/icons/dots.svg';
  import iconSvg from '../IconSvg/IconSvg.vue'
export default {
    components:{
     
     iconSvg,
    },
props: {
    text: {
        type: String,
        default: 'Button!',
        required: true,
    },
    className: {
        type: String,
        default: 'button',
        required: true,
    },
    id: {
        type: String,
        required: true,
    }
},
data() {
        return {
            classNameSvg: 'clicker',
            nameSvg: '#dots',
            menuVisible: false,
        }
    },


   methods: {
    openMenu(){
          this.menuVisible = !this.menuVisible;
        }
   }
}
</script>

<style lang="scss">
  @import '@/sass/color.scss';


/* main styles */

.btn-addittionaly{
position: relative ;
display: none;
}


.btn-update{
  
    z-index: 3;
    position: absolute;
    top: 100%;
    right: 0;
    background-color: $bg-secondary;
    box-shadow: 0px 0px 4px rgba(0, 0, 0, 0.25);
    padding: 4px;

}

.update-menu__list{
    list-style: none;
    
}

.update-menu__item {
    padding: 8px;
}
.update-menu__link {
    color:$font-primaryDefault;
    text-decoration: none;
    background-color:none;
    &:hover{
        text-decoration: underline;
    }
    
}
.update-menu__link-r{
    color:$font-error;
}



</style>
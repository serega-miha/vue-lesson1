
 <template>
  <div>
    <div class="btn-user" @click="menuVisible = !menuVisible">
        <a class="button button-user"> 
            <img class="menu-profile-avatar avatar-img" v-bind:src="srcImg" alt="img profile">
            <iconSvg
                :className="classNameSvg"
                :nameSvg="nameSvg"
            ></iconSvg>
        </a> 
        <div class="btn-user__menu" v-show="menuVisible">
        <ul class="user__menu-list">
            <li class="user__menu-item">
                <a href="#" class="user__menu">Профиль</a>
            </li>
            <li class="user__menu-item">
                <a href="#" class="user__menu">Выход</a>
            </li>
        </ul>
      
        
    </div>
    </div>
    
   </div>
 </template>
 <script>
   import imgProfile from '@/assets/img/logo-icon.png'
   import iconSvg from '../IconSvg/IconSvg.vue'
 export default {
    components:{
        iconSvg,
    },
  
     data() {
         return {
            srcImg: imgProfile,
            nameSvg: '#drop-down',
            classNameSvg: '',
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
    
.btn-user{
    position: relative;
}
.btn-user__menu{
    
    z-index: 3;
    position: absolute;
    top: 101%;
    right: 0;
    background-color: $bg-secondary;
    box-shadow: 0px 0px 4px rgba(0, 0, 0, 0.25);
    // padding: 4px;

}


.user__menu-list {
    list-style: none;
}
.user__menu-item {
    padding: 16px 16px 16px 16px;
    &:first-child{
        padding-bottom: 8px;
        
    }
    &:last-child{
        padding-top: 8px;
        
    }
    
}
.user__menu{
    color:$font-primaryDefault;
    text-decoration: none;
    background-color:none;
    &:hover{
        text-decoration: underline;
    }
    
    
}

//general styles
.avatar-img{
    width: 24px;
    height: 24px;
    border-radius: 50%;
    margin: 0px 14px 0px 0px;
}


 </style>
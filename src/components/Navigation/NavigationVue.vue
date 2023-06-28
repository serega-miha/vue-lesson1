
 <template>
    <nav class="menu">
    <ul class="menu__list">
        <li class="menu__item" :key="index" v-for="(info, index) in infoBtns">
            <buttonStandart :text="info.name" :className="className" :id="info.id"></buttonStandart>
        </li>

    </ul>

    <iconUserButton></iconUserButton>
   
   
</nav>  
  </template>

  <script>
  import '@/assets/icons/drop-down.svg';
  import iconUserButton from '../IconUserButton/iconUserButton.vue';
  import buttonStandart from '../Button/ButtonStandart.vue';

  export default {
    components: {
        iconUserButton,
        buttonStandart,
    },
  
      data() {
          return {
            infoBtns: [
                {name: 'Проекты', id: 'projects'},
                {name: 'Задачи', id: 'tasks'},
                {name: 'Пользователи', id: 'users'},
            ],
            className: 'button button-nav',
            
          }
      },
  
  }
  </script>

  <style lang="scss">
 @import './style.scss';

  </style>
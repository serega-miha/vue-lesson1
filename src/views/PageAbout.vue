
<template>
      <div class="wrapper">
        <header class="header">
            <navigation></navigation>
        </header>
        <main class="main">
            <div class="page-profile profile">
                <div class="profile-container">
                    <div class="profile__foto">
                        <img v-bind:src="srcImg" >
                    </div>
                    <div class="profile__info">
                        <div class="info-name">{{name}}</div>
                        <div class="info-about">
                            <label >О себе:</label>
                            <p>{{ aboutText }}</p>
                            </div>
                    </div>
                </div>
            </div>

        </main>
       
        
    </div>

  </template>
  
  <script>
    import imgProfile from '@/assets/img/picture1.png'
    import navigation from '../components/Navigation/NavigationVue.vue';

  export default {
    components: {
        navigation,
       
    },

    data() {
      return {
        srcImg: imgProfile,
        name: 'Котов Семен Васильевич',
        aboutText: 'Далеко-далеко за словесными горами в стране гласных и согласных живут рыбные тексты. Вдали от всех живут они в буквенных домах на берегу Семантика большого языкового океана. Маленький ручеек Даль журчит по всей стране и обеспечивает ее всеми необходимыми правилами. Эта парадигматическая страна, в которой жаренные члены предложения залетают прямо в рот. Даже всемогущая пунктуация не имеет власти над рыбными текстами, ведущими безорфографичный образ жизни. Однажды одна маленькая строчка рыбного текста по имени Lorem ipsum решила выйти в большой мир грамматики. Великий Оксмокс предупреждал ее о злых запятых, диких знаках вопроса и коварных точках с запятой, но текст не дал сбить себя с толку. Он собрал семь своих заглавных букв, подпоясал инициал за пояс и пустился в дорогу. Взобравшись на первую вершину курсивных гор, бросил он последний взгляд назад, на силуэт своего родного города Буквоград, на заголовок деревни Алфавит и на подзаголовок своего переулка Строчка. Грустный риторический вопрос скатился по его щеке и он продолжил свой путь. По дороге встретил текст рукопись. Она предупредила его: «В моей стране все переписывается по несколько раз. Единственное, что от меня осталось, это приставка «и». Возвращайся ты лучше в свою безопасную страну». Не послушавшись рукописи, наш текст продолжил свой путь. Вскоре ему повстречался коварный составитель рекламных текстов, напоивший его языком и речью и заманивший в свое агенство, которое использовало его снова и снова в своих проектах. И если его не переписали, то живет он там до сих пор. Далеко-далеко за словесными горами в стране гласных и согласных живут рыбные тексты. Вдали от всех живут они в буквенных домах на берегу Семантика большого языкового океана. Маленький ручеек Даль журчит по всей стране и обеспечивает ее всеми необходимыми правилами. Эта парадигматическая страна, в которой жаренные члены предложения залетают прямо в рот. Даже всемогущая пунктуация не имеет власти над рыбными текстами, ведущими безорфографичный образ жизни. Однажды одна маленькая строчка р.',

      }
    },
  
    computed: {
    
    },
    watch: {
    },
  
    methods: {
     
    }
  }
  </script>
  
  <style lang="scss">
    @import '../sass/color.scss';
  

.main{
    flex: 1 1 auto;
    width: 100%;
    min-height: 100%;
    overflow: hidden;
    display: flex;
    flex-direction: column;
   }


.page-profile {
    padding: 20px;
}
.profile {
   
}
.profile-container {
    display: flex;
}
.profile__foto {
    margin: 0px 20px 0px 0px;
    
}
.profile__info {
}
.info-name {
    font-size: 24px;
    font-weight: 600;
    margin: 0px 0px 33px 0px;
    
}
.info-about {
    label{
        color: $font-disabled;
        margin: 0px 0px 24px 0px;
        
    }
}
  </style>
  
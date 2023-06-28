
 <template>
     <div class="search-project__search">
            <input :placeholder="namePlaceholder" type="search">
            <a>
                <iconSvg
                :className="classNameSvg"
                :nameSvg="nameSvg"
            ></iconSvg>
            </a>
        </div>
 </template>

 <script>
    import iconSvg from '../IconSvg/IconSvg.vue'

 export default {
    components:{
     iconSvg,
 },
    props: {
        namePlaceholder: {
            type: String,
            required: true,
    },
   
},

    
     data() {
         return {
            nameSvg: '#dots',
            classNameSvg: '',
         }
     },
 
 }
 </script>

 <style lang="scss">
 

 .search-project__search {
    
    border: 1px solid grey;
    margin: 20px;
    display: flex;
    justify-content: space-between;
    border-radius: 4px;
    height: 42px;

    a{
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 0px 10px;
        cursor: pointer;
    }
    input{
       flex: 1 1 auto;
       padding: 0px 10px
    }
    svg{
        
        width: 24px;
        height: 24px;
    }
}
 </style>
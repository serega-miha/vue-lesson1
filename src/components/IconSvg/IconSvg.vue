
 <template>
    <svg :class="className">
        <use :xlink:href="nameSvg" />
    </svg>
 </template>

 <script>
 export default {
    props: {
    nameSvg: {
        type: String,
        required: true,
    },
    className: {
        type: String,
        required: true,
    }
},
 }
 </script>
  <style>
 
 </style>
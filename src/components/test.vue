<template >
    <div>
        {{score}}
    <p id="add">{{i+1}}. {{quest[i].question}} </p>
   

      <p> 
          <ul>
    <li v-for="(item, index) in quest[i].answers" :key="index" @click="showAns()" :class="select ? check(item) : ''">  {{item.answer}}  </li>
     
     </ul>
     </p> 
    </div>
</template>






<script>


export default {
    name:'Test',
    props:{
     quest : Array,
     i : Number,
     select : Boolean,
     
    },

    data (){
        return{
         
   
     
          
        }
    },

methods: {
    showAns(){
   this.select = true;
   
    },

    check(condition){
            if(condition.correct){
                // console.log('true')
                return 'correct'
            } else {
                // console.log('false')
                return 'incorrect'
            }
    }

},
    
}
</script>



<style>
  #user-goal ul {
list-style-type: none;
}

li.incorrect{
 color: white
}

li.correct{
 color: lawngreen;
 background-color: honeydew;
 

}

</style>
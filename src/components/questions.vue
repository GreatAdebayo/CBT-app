<template>
<div>
<header>
      <h1>CBT Test</h1>
    </header>
    <section id="user-goal">
      <h5>Questions</h5>
    
      

     <p><Test :quest="quest" :i="i" :select="select"/> </p> 

     <button @click="backQue"><strong>Back</strong></button>
      <button @click="nextQue"><strong>Next</strong></button> 
    </section>

      <header>
          <h6>@Great</h6>
      </header>
</div>
</template>



<script>
import quest from './quest.js'
import Test from'./test.vue'
export default {
    name:'Question',
    components: {
      Test
    },

    data() {
        return {
    
      i : 0,

   quest:quest,
 select : false
    
     
        }
    },

    methods : {

nextQue(){
    ++ this.i 
   this.select = false;
    
},
backQue(){
    --this.i
},
  showOpt (){



  },
  showAns (){
    console.log(this.name)
  }

    }
}

</script>







<style scoped>
* {
  box-sizing: border-box;
}

html {
  font-family: 'Jost', sans-serif;
}

body {
  margin: 0;
}

header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem auto;
  border-radius: 10px;
  padding: 1rem;
  background-color: #4fc08d;
  color: white;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}

#user-goal {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}

#user-goal h5 {
  font-size: 2rem;
  border-bottom: 2px solid #ccc;
  color: #4fc08d;
  margin: 0 0 1rem 0;
}



#user-goal p {
  font-size: 1.25rem;
  font-weight: bold;
  border: 1px solid #4fc08d;
  background-color: #4fc08d;
  color: white;
  padding: 0.5rem;
  border-radius: 25px;
}

#user-goal input {
  font: inherit;
  border: 1px solid #ccc;
}

#user-goal input:focus {
  outline: none;
  border-color: #4fc08d;
  background-color: #d7fdeb;
}

#user-goal button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #d7fdeb;
  background-color: #4fc08d;
  color: white;
  padding: 0.5rem 1.5rem;
  outline-color: white;
  margin-right: 4rem;
  margin-left: 4rem 
  
}

#user-goal button:hover,
#user-goal button:active {
  background-color: #4fc08d;
  border-color:#d7fdeb; 
  
}

</style>
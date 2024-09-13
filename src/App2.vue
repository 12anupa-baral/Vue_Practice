<!-- option api -->

<script>
export default{
  data(){
    return{
 name:'Anupa Baral',
 status:'pending',
 tasks:['task 1','task 2','task 3'],
 link:'https://google.com',
 
    }
   
   
  },
  methods:{
    toggleStatus(){
      if(this.status === 'active'){
        this.status = 'pending';
      }
      else if( this.status === 'pending'){
        this.status = 'inactive';
      }
      else{
        this.status = 'active';
      }
    }
  }
}
</script>

<template>
  <h1>{{name}}</h1>

  <!-- conditional rendering -->
  <p v-if="status === 'active'"> User is active</p>
  <p v-else-if="status === 'pending'"> User is pending</p>
  <p v-else> User is inactive</p>

  <!-- for loop   -->
  <h3>Tasks:</h3> 
  <ul>
    <li v-for="task in tasks" key="task">{{ task }}</li>
  </ul>

  <!-- dynamic link -->
  <!-- <a v-bind:href="link">Click for google</a> -->
<br/>
  <!-- shortform -->
  <a :href="link">Click for google</a>
<br/>

<!-- event hsndling -->
  <!-- <button v-on:click="toogleStatus">Change Status</button> -->

  <!-- shortform -->
  <button @click="toggleStatus">Change Status</button>

  
</template>

<style scoped>
h1{
  color:red;
}
</style>


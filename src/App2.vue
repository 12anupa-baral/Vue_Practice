<!-- composition api -->

<script>

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
  <button @click="toogleStatus">Change Status</button>

  
</template>

<style scoped>
h1{
  color:red;
}
</style>


<script setup>
// VueJS Crash Course 2024
// Composition  
import {ref} from 'vue';
    const name = ref('Jonh Doe');
    const status = ref('active');
    const tasks = ref(['Task one','Task Two','Task Three']);
  
    const toggleStatus = () => {
      if (status.value === 'active') {
        status.value = 'pending';
      } else if (status.value === 'pending') {
        status.value = 'inactive';
      }  else {
        status.value = 'active';
      }
    }
</script>

<template>
 <h1>{{ name }}</h1>
 <p v-if="status === 'active'">User is active</p>
 <p v-else-if="status === 'pending'">User is pending</p>
 <p v-else>User is inactive</p>
 <h3>Task:</h3>
 <ul>
  <li v-for="task in tasks" :key="task">{{ task }}</li>
 </ul>
 <!---<a v-bind:href="link">Click for Google</a>-->
 <!-- <a href="link">Click for Google</a> -->
<br>
 <!-- <button v-on:click="toggleStatus">Change Status</button> -->
 <button @click="toggleStatus">Change Status</button>
</template>



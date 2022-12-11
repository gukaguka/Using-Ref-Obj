<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 >OUTPUT COURSE GOAL : <h3 :class="goalObject.toggleGoal">{{  goalObject.courseGoal }}</h3></h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button  @click='onToggleGoal'>Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import {ref} from 'vue';
export default {
  setup(){
  const goalObject = ref({
  courseGoal : 'laern vue',
  toggleGoal : 'show'
  });

 function onToggleGoal(){
    goalObject.value.toggleGoal === "show" ? goalObject.value.toggleGoal = "hide" :  goalObject.value.toggleGoal = "show";
 }
  return { goalObject, onToggleGoal };

  },
}
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
.show {
  visibility: visible;
}

.hide {
  visibility: hidden;
}
</style>
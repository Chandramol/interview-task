<template>
  <TaskOne />
  <br>
  <TaskTwo />
</template>

<script>
import TaskOne from './components/TaskOne.vue';
import TaskTwo from './components/TaskTwo.vue';

export default {
  name: 'App',
  components: {
    TaskOne,
    TaskTwo
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

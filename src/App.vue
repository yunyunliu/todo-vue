<template>
  <div id='id'>
    <h1>todo list</h1>
    <ul>
      <li>
        <to-do-item label="first todo item" :done="false"></to-do-item>
      </li>
      <li>
        <to-do-item label="second todo item" :done="true"></to-do-item>
      </li>
      <li>
        <to-do-item label="third todo item" :done="true"></to-do-item>
      </li>
      <li>
        <to-do-item label="fourth todo item" :done="false"></to-do-item>
      </li>
    </ul>
  </div>
</template>

<script>
  import ToDoItem from './components/ToDoItem.vue'
  export default {
    name: 'App',
    components: { ToDoItem }
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

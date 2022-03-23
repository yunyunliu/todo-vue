<template>
  <div>
    <label for="todo-item">{{label}}</label>
    <input type='checkbox' id="todo-item" />
  </div>
</template>

<script>
  export default {
    props: {
      label: { required: true, type: String },
      done: { default: false, type: Boolean }
    }
  }
</script>

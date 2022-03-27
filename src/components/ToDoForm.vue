<template>
  <form @submit.prevent="onSubmit">
    <label for="add-todo-input">What to do?</label>
    <input id="add-todo-input" />
    <button>Add</button>
  </form>
</template>

<script>
  export default {
    methods: {
      onSubmit() {
        console.log('form submitted')
      }
    }
  };
</script>

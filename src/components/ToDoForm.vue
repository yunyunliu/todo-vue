<template>
  <form @submit.prevent="onSubmit">
    <label for="add-todo-input">What to do?</label>
    <input id="add-todo-input" v-model.lazy.trim="label" />
    <button>Add</button>
  </form>
</template>

<script>
  export default {
    data() {
      return {
        label: ''
      }
    },
    methods: {
      onSubmit() {
        if (this.label === '') return;
        this.$emit('todo-added', this.label)
        this.label = '';
      }
    }
  };
</script>

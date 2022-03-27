<template>
  <form @submit.prevent="onSubmit">
    <h2>
      <label for="add-todo-input">What to do?</label>
    </h2>
    <input id="add-todo-input" type="text" v-model.lazy.trim="label" />
    <button class="btn btn__primary btn__lg">Add</button>
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

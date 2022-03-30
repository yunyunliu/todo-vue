<template>
  <form @submit.prevent="onSubmit">
    <h2 class="label-wrapper">
      <label for="new-todo-input" class="label__lg">
        What to do?
      </label>
    </h2>
    <input
        id="new-todo-input"
        type="text"
        name="new-todo"
        v-model.lazy.trim="label"
        class="input__lg"
      />
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

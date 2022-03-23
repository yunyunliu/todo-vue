<template>
  <div>
    <label :for="id">{{label}}</label>
    <input type='checkbox' :checked="isDone" :id="id" />
  </div>
</template>

<script>
  import uniqueId from 'lodash.uniqueid';
  export default {
    props: {
      label: { required: true, type: String },
      done: { default: false, type: Boolean }
    },
    data() {
      return {
        isDone: this.done,
        id: uniqueId('todo-')
      }
    }
  }
</script>

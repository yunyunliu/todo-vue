<template>
  <div>
    <label :for="id">{{label}}</label>
    <input type='checkbox' :checked="isDone" :id="id" />
  </div>
</template>

<script>
  export default {
    props: {
      label: { required: true, type: String },
      done: { default: false, type: Boolean },
      id: { required: true, type: String }
    },
    data() {
      return {
        isDone: this.done
      }
    }
  }
</script>

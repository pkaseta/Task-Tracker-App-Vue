<template>
  <h3>{{task.text}}
    <i class="fas fa-times"></i>
  </h3>
  <p>{{task.day}}</p>

</template>

<script>
export default {
  name: "SingleTask",
  props:
      {
        task: Object
      }
}
</script>

<style scoped>
  .fas
  {
    color: red;
    margin-left: 10px;
  }
</style>
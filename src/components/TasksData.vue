<template>
  <div v-for="task in tasks"
       :key="task.id">
    <SingleTask @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>

<script>
import SingleTask from "./SingleTask"
export default {
  name: "TasksData",
  props:
  {
    tasks: Array
  },
  components:
  {
    SingleTask
  },
  emits: ['delete-task']
}
</script>

<style scoped>

</style>
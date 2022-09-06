<template>
  <div v-for="task in tasks"
       :key="task.id">
    <SingleTask :task="task" />
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
  }
}
</script>

<style scoped>

</style>
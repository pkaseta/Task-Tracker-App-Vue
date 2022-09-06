<template>
  <div class="tasks-container">
    <h3>{{task.text}}
      <i @click="onDelete(task.id)" class="fas fa-times"></i>
    </h3>
    <p>{{task.day}}</p>
    <p>
      <strong>
        Reminder: {{ task.reminder ? 'Yes' : 'No' }}
      </strong>
    </p>
  </div>
</template>

<script>

export default {
  name: "SingleTask",
  props:
      {
        task: Object
      },
  methods:
      {
        onDelete(id) {
          this.$emit("delete-task", id)
        }
      }
}
</script>

<style scoped>
  .fas
  {
    color: red;
    margin-left: 10px;
  }
  .tasks-container {
    padding: 5px;
    border-radius: 5px;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
</style>
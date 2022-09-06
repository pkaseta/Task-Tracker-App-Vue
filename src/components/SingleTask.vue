<template>
  <div class="tasks-container">
    <h3 class="tasks-title">{{task.text}}
      <div @click="onDelete(task.id)" class="tasks-content">
      <i class="fas fa-times"></i>
      </div>
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
  }
  .tasks-container {
    padding: 5px;
    border-radius: 5px;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    background: #2c3e50;
    color: #fff;
  }
  .tasks-title {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  .tasks-content {
    width: 30px;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid white;
    border-radius: 5px;
  }
</style>
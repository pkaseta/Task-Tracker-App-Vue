<template>
 <PageHeader title="Task tracker"/>
  <TaskData @delete-task="deleteTask" :tasks="tasks" />
</template>

<script>
import PageHeader from "./components/PageHeader"
import TaskData from "./components/TasksData"

export default {
  name: 'App',
  components: {
    PageHeader,
    TaskData
  },
  data ()
  {
    return {
      tasks: [],
    }
  },
  methods:
      {
        deleteTask (id)
        {
          if(confirm('Are you sure you want to delete this task?')) {
            this.tasks = this.tasks.filter(task => task.id !== id)
          }
        }
      },
  created()
  {
    this.tasks =
        [
          {
            id: 1,
            text: "Appointment",
            day: "March 1st at 2:30pm",
            reminder: true,
          },
          {
            id: 2,
            text: "Meeting at school",
            day: "March 3rd at 1:30pm",
            reminder: true,
          },
          {
            id: 3,
            text: "Food Shopping",
            day: "March 3rd at 11:00am",
            reminder: false,
          }
        ]
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

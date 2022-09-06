<template>
  <button
      :style="{background: color}"
      @click="onClick()"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "TaskButton",
  props: {
    text: String,
    color: String
  },
  methods:
  {
    onClick()
    {
      console.log("onClick called")
    }
  }
}
</script>

<style scoped>

</style>
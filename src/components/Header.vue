<template>
  <header>
    <h1>{{ title }}</h1>
    <v-btn
      @click="$emit('toggle-add-task-form')"
      :color="showAddTaskForm ? 'red' : 'green'"
    >
      {{ showAddTaskForm ? "Close" : "Add Task" }}
    </v-btn>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
    showAddTaskForm: Boolean,
  },
  emits: ["toggle-add-task-form"],
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>

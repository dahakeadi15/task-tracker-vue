<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggle-add-task-form')"
      :text="showAddTaskForm ? 'Close' : 'Add Task'"
      :color="showAddTaskForm ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: String,
    showAddTaskForm: Boolean,
  },
  components: {
    Button,
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

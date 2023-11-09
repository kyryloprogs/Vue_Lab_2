<template>
  <div>
    <h4 class="text-center my-3 pb-3">To Do App</h4>
    <AddTaskForm></AddTaskForm>
    <TaskList ref="taskList"></TaskList>
  </div>
</template>

<script>
import AddTaskForm from "./components/AddTaskForm.vue";
import TaskList from "./components/TaskList.vue";

export default {
  components: {
    AddTaskForm,
    TaskList,
  },
};
</script>

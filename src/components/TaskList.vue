<template>
  <table class="table mb-4">
    <thead>
      <tr>
        <th scope="col">No.</th>
        <th scope="col">Todo item</th>
        <th scope="col">Status</th>
        <th scope="col">Actions</th>
      </tr>
    </thead>
    <tbody>
      <task-item
        v-for="(task, index) in tasks"
        :key="index"
        :task="task"
        @deleteTask="deleteTask(index)"
      ></task-item>
    </tbody>
  </table>
</template>

<script>
import TaskItem from "./TaskItem.vue";

export default {
  data() {
    return {
      tasks: [
        { text: "Buy groceries for next week", status: "In progress" },
        { text: "Renew car insurance", status: "In progress" },
        { text: "Sign up for an online course", status: "In progress" },
      ],
    };
  },
  components: {
    TaskItem,
  },
  methods: {
    deleteTask(index) {
      this.tasks.splice(index, 1);
    },
  },
};
</script>

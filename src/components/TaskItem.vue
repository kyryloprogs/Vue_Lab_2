<template>
  <tr>
    <th scope="row">{{ taskNo }}</th>
    <td>{{ task.text }}</td>
    <td>{{ task.status }}</td>
    <td>
      <button @click="deleteTask" class="btn btn-danger">Delete</button>
      <button class="btn btn-success ms-1">Finished</button>
    </td>
  </tr>
</template>

<script>
export default {
  props: ["task", "taskNo"],
  methods: {
    deleteTask() {
      this.$emit("deleteTask");
    },
  },
};
</script>

<template>
  <div class="form-outline">
    <input type="text" v-model="newTask" class="form-control" />
    <label class="form-label" for="form1">Enter a task here</label>
    <button @click="addTask" class="btn btn-primary">Save</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTask: "",
    };
  },
  methods: {
    addTask() {
      if (this.newTask.trim() !== "") {
        this.$root.$refs.taskList.tasks.push({
          text: this.newTask,
          status: "In progress",
        });
        this.newTask = "";
      }
    },
  },
};
</script>

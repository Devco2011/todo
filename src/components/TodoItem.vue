<template>
  <div>
    <h2 :class="{ completed: todo.complete }">{{ todo.name }}</h2>
    <button @click="handleClick">{{ buttonText }}</button>
  </div>
</template>

<script>
export default {
  props: ["todo"],

  methods: {
    handleClick() {
      this.$emit("status-change", this.todo);
    },
  },

  computed: {
    buttonText() {
      return this.todo.complete ? "Mark inclomplete" : "Mark Completed";
    },
  },
};
</script>

<style scoped>
div {
  width: 50%;
  border: 2px solid red;
  margin: 15px;
  padding: 10px;
  text-align: center;
}
.completed {
  text-decoration: line-through;
  text-decoration-color: tomato;
}
</style>
<template>
  <div>
    <h2>{{ todo.name }}</h2>
    <button>Mark Completed</button>
  </div>
</template>

<script>
export default {
  props: ["todo"],
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
</style>
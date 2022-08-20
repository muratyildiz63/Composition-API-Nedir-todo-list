<template>
  <div class="w-full h-full text-white">
    <h3 class="w-full flex mb-5">Yemek Listesi</h3>
    <addTodo />
    <todoList />
  </div>
</template>

<script>
import addTodo from "./components/addTodo";
import todoList from "./components/todoList";
export default {
  components: {
    addTodo,
    todoList,
  },
};
</script>


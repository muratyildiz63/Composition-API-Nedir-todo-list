<template>
  <div class="w-full h-full text-white">
    <h3 class="w-full flex mb-5">Yemek Listesi</h3>
    <addTodo :addTodo="addTodo" />
    <todoList :foodList="foodList" />
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
import addTodo from "./components/addTodo.vue";
import todoList from "./components/todoList.vue";
export default {
  components: {
    addTodo,
    todoList,
  },

  setup() {
    const foodList = ref([
      {
        id: 1,
        foodName: "Lahmacun",
      },
    ]);

    const addTodo = (event) => {

      
      foodList.push({
        id: new Date().getTime(),
        foodName: event,
      });
    };

    return {
      foodList,
      addTodo
    };
  },
};
</script>


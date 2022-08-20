<template>
  <div class="w-full h-full text-white">
    <h3 class="w-full flex mb-5">Yemek Listesi</h3>
    <addTodo :addTodo="addTodo" />
    <todoList :foodList="foodList"  @delete-item="deleteItems"/>
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
      foodList.value.push({
        id: new Date().getTime(),
        foodName: event,
      });
    };
    const deleteItems =(event)=>{
      console.log(event)
    }

    return {
      foodList,
      addTodo,
      deleteItems
    };
  },
};
</script>


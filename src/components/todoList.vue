<template>
  <div class="flex justify-center">
    <div class="rounded-lg w-96">
      <TodoListItem @delete-item="$emit('delete-item', $event)"  v-for="food in foodListt" :key="food.id" :item="food" />
      <small>{{foodListt.length}} adet item vardır</small>
      <summary />
    </div>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem.vue";
import summary from "./summary.vue";
import { computed } from '@vue/runtime-core';
export default {
  props: ["foodList"],
  components: {
    TodoListItem,
    summary,
  },

  setup(props){ 
      const foodListt = computed(()=>props.foodList)

      return{
        foodListt
      }
  }
};
</script>
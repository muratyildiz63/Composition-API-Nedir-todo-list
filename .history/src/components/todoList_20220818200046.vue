<template>
  <div class="flex justify-center">
    <div class="rounded-lg w-96">
      <TodoListItem v-for="food in foodList" :key="food.id" :item="food" />
      <small>{{foodList.length}} adet item vardır</small>
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
      const foodList = computed(()=>props.foodList)

  }
};
</script>
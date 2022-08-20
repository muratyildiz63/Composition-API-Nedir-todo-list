<template>
  <div class="flex justify-center">
    <div class="rounded-lg w-96">
      <TodoListItem v-for="food in foodList" :key="food.id" :item="food" />
      <small>X adet item vardır</small>
      <summary />
    </div>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem.vue";
import summary from "./summary.vue";
export default {
  props: ["foodList"],
  components: {
    TodoListItem,
    summary,
  },
};
</script>
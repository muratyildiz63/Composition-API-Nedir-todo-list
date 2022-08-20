<template>
  <div class="flex justify-center">
    <div class="rounded-lg w-96">
    <TodoListItem  v-for="food in  foodList" :key="food.id" />
    </div>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem.vue"
export default{
    props:["foodList"],
    components:{
        TodoListItem
    }
}

</script>
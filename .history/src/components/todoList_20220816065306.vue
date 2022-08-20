<template>
  <div class="flex justify-center">
    <div class="rounded-lg w-96">
    <TodoListItem />
    </div>
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem.vue"
export default{
    components:{
        TodoListItem
    }
}

</script>
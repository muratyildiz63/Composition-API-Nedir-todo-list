<template>
  <div
    aria-current="true"
    class="
      bg-black
      flex
      justify-between
      mb-2
      px-2
      py-2
      border border-gray-200
      w-full
      rounded-lg
      text-white
      cursor-pointer
      even:bg-gray-700
    "
  >
    <label :for="'item' + item.id">
      <input type="checkbox" name="" :id="'item' + item.id" />
      {{ item.foodName }}
    </label>
    <button @click="deleteItem" class="bg-orange-50 px-1 text-black">
      Sil
    </button>
  </div>
</template>

<script>
export default{
    props:["item"]
}

setup(props  , {emit}) {
  
const deleteItem =()=>{
  emit("delete-item",props.item)
}
  return{
    deleteItem
  }
}


</script>
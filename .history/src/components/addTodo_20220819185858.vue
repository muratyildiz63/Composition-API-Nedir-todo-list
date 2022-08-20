<template>
  <section>
    <input
      type="text"
      class="
        form-control
        block
        w-full
        px-3
        mb-5
        py-1.5
        text-base
        font-normal
        text-gray-700
        bg-white bg-clip-padding
        border border-solid border-gray-300
        rounded
        transition
        ease-in-out
        m-0
        focus:text-gray-700
        focus:bg-white
        focus:border-blue-600
        focus:outline-none
      "
      id=""
      placeholder="Yemek Ekle"
      @keydown="newItem"
    />
  </section>
</template>

<script>

export default {
  props:{
    addTodo
  },
  setup(props) {
 const newItem= (event)=>{
  props.item(event.target.value)
  }
  return{
    newItem
  } 

}
}

</script>
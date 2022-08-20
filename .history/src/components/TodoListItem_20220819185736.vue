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
    <label for="compluted">
      <input type="checkbox" @keydown="newItem" name="" id="compluted" />
      {{ item.foodName }}
    </label>
    <button class="bg-orange-50 px-1 text-black">Sil</button>
  </div>
</template>

<script>
export default{
    props:["item"]
}


</script>
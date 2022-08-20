<template>
  <div class="w-full h-full text-white">
    <h3 class="w-full flex mb-5">Yemek Listesi</h3>

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
        focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none
      "
      id="exampleFormControlInput1"
      placeholder="Yemek Ekle"
    />



</section>


    <div class="flex justify-center">
      <div class="rounded-lg w-96">
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
            <input type="checkbox" name="" id="compluted" /> deneme
          </label>
          <button class="bg-orange-50 px-1 text-black">Sil</button>
        </div>

        
      </div>
    </div>
  </div>
</template>


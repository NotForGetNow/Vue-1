<script setup>
defineProps({
  image: String,
  name: String,
  price: Number,
  isAdded: Boolean,
  isFavourite: Boolean,
  onClickAdd: Function
})
</script>


<template>
  <div class="border p-10 rounded-xl relative transition hover:-translate-y-2 hover:shadow-xl">
    <img :src="isFavourite ? '/like-2.svg' : '/like-1.svg'" class="absolute top-5 left-5" alt="" />
    <img :src="image" alt="" />
    <p class="mt-5 mb-3">{{ name }}</p>
    <div class="flex justify-between">
      <div class="flex flex-col">
        <span class="uppercase text-gray-400">цена:</span>
        <span class="font-bold">{{ price }} тенге</span>
      </div>
      <img @click="onClickAdd" :src="isAdded ? 'checked.svg' : 'plus.svg'" alt="" />
    </div>
  </div>
</template>
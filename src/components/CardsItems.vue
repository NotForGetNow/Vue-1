<script setup>
import Card from './CardItem.vue'

defineProps({
  items: Array
})

const onClickAdd = () => {
  alert('Добавлено')
}
</script>

<template>
  <div class="p-10 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-4 gap-5">
    <Card
      v-for="item in items"
      :key="item.id"
      :image="item.imageUrl"
      :name="item.title"
      :price="item.price"
      :isAdded="false"
      :isFavourite="false"
      :onClickAdd="onClickAdd"
    />
  </div>
</template>
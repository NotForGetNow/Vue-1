<script setup>
import Header from './components/HeaderComponent.vue'
import Card from './components/CardItem.vue'
import Cards from './components/CardsItems.vue'
import Drawer from './components/DrawerComponent.vue'
</script>

<template>
  <div class="w-4/5 m-auto bg-white rounded-xl shadow-xl mt-14 pb-2">
    <Drawer />
    <Header />
    <!-- лягушка -->
    <div class="">

    </div>
    <h1 class="font-bold p-10 text-4xl">Все кроссовки</h1>
    <!-- поиск -->
    <Cards />
  </div>
</template>

<style scoped>
</style>
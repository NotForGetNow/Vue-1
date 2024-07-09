<script setup>
import Header from './components/HeaderComponent.vue'
import Card from './components/CardItem.vue'
import Cards from './components/CardsItems.vue'
import Adidas from './components/AdidasCart.vue'
import Search from './components/SearchComponent.vue'
import { onMounted, ref, watch } from 'vue'
import axios from  'axios'
// import Drawer from './components/DrawerComponent.vue'

const items = ref([])
const sortBy = ref([])

const onChangeSelect = (event) => {
  sortBy.value = event.target.value
}

onMounted(async () => {
  try {
    const { data } = await axios.get('https://269b3b45e08bcd1a.mokky.dev/items' + sortBy.value)
    items.value = data
  } catch (error) {
    console.log(error)
  }
})

watch(sortBy, async () => {})

</script>

<template>
  <!-- <Drawer /> -->
  <div class="w-4/5 m-auto bg-white rounded-xl shadow-xl mt-14 pb-2">
    <Header />
    <div class="flex items-center flex-col">
      <Adidas />
    </div>

    <Search /> 
    <Cards :items="items" />
  </div>
   
</template>

<style scoped>
</style>
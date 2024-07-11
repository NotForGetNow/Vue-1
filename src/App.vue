<script setup>
import Header from './components/HeaderComponent.vue'
import Card from './components/CardItem.vue'
import Cards from './components/CardsItems.vue'
import Adidas from './components/AdidasCart.vue'
import Search from './components/SearchComponent.vue'
import Drawer from './components/DrawerComponent.vue'

import { onMounted, reactive, ref, watch, provide} from 'vue'
import axios from 'axios'

const items = ref([])
const openCart = ref(false)
const filters = reactive({
  sortBy: 'title',
  searchBy: ''
})
const openDrawer = () => {
  openCart.value = true
}
const closeDrawer = () => {
  openCart.value = false
}

provide('closeDrawer', closeDrawer)

const fetchitems = async () => {
  try {
    const params = {
      sortBy: filters.sortBy,
    }
    if (filters.searchBy) {
      params.title = filters.searchBy
    }
    const { data } = await axios.get('https://eefe547f0ab3c587.mokky.dev/items', {
      params
    })
    items.value = data

  } catch (error) {
    console.log(error)
  }
}

const onChangeSelect = (event) => {
  filters.sortBy = event.target.value
}

const onChangeInput = (event) => {
  filters.searchBy = `*${event.target.value}*`
}

onMounted(fetchitems)
watch(filters, fetchitems)

</script>

<template>
  <Drawer v-if="openCart" />
  <div class="w-4/5 m-auto bg-white rounded-xl shadow-xl mt-14 pb-2">
    <Header :openDrawer="openDrawer" />

    <div class="flex items-center flex-col">
      <Adidas />
    </div>

    <Search :onChangeSelect="onChangeSelect" :onChangeInput="onChangeInput" /> 

    <Cards :items="items" />
  </div>
   
</template>

<style scoped>
</style>
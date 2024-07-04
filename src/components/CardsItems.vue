<script setup>
import Card from './CardItem.vue'

const onClickAdd = () => {
    alert('Добавлено')
}
</script>

<template>
    <div class="p-10 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-4 gap-5">
        <Card
            image="/sneakers/sneakers-1.jpg"
            name="Мужские Кроссовки Nike Blazer Mid Suede"
            :price="12999"
            :isAdded="false"
            :isFavourite="true"
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-2.jpg" 
            name="Мужские Кроссовки Nike Air Max 270" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-3.jpg" 
            name="Мужские Кроссовки Nike Blazer Mid Suede" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-4.jpg" 
            name="Кроссовки Puma X Aka Boku Future Rider" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-5.jpg" 
            name="Мужские Кроссовки Under Armour Curry 8" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-6.jpg" 
            name="Мужские Кроссовки Nike Kyrie 7" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-7.jpg" 
            name="Мужские Кроссовки Jordan Air Jordan 11" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-8.jpg" 
            name="Мужские Кроссовки Nike LeBron XVIII" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-9.jpg" 
            name="Мужские Кроссовки Nike Lebron XVIII Low" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-1.jpg" 
            name="Мужские Кроссовки Nike Blazer Mid Suede" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-4.jpg" 
            name="Кроссовки Puma X Aka Boku Future Rider" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
        <Card image="/sneakers/sneakers-10.jpg" 
            name="Мужские Кроссовки Nike Kyrie Flytrap IV" 
            :price="12999" 
            :isFavorite="false"
            :isAdded="false"  
            :onClickAdd="onClickAdd"
        />
    </div>
</template>
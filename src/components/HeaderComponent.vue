<template>
    <header class="flex justify-between border-b bg-slate-300 px-10 py-5">
        <div class="flex gap-4 item-center">
            <img class="w-10" src="/logo.png" alt="logo">
            <div>
                <h2 class="text-x1 font-bold uppercase">Vue Sneakers</h2>
                <p class="to-slate-400">Магазин лучших кроссовок</p>
            </div>
        </div>
        <ul class="flex items-center gap-10">
            <li class="flex items-center gap-3 cursor-pointer to-gray-500 hover:text-black">
                <img src="/cart.svg" alt="">
                <p>1205 тенге</p>
            </li>
            <li class="flex items-center gap-3 cursor-pointer to-gray-500 hover:text-black">
                <img src="/heart.svg" alt="">
                <p>Закладки</p>
            </li>
            <li class="flex items-center gap-3 cursor-pointer to-gray-500 hover:text-black">
                <img src="/profile.svg" alt="">
                <p>Профиль</p>
            </li>
        </ul>        
    </header>
</template>
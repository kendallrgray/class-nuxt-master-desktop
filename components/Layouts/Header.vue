<template>
<header class="bg-gray-500 text-white px-4 py-3 flex justify-between flex-row"
> This is the header 
<nav>
    <ul class="flex flex-row gap-4 px-4">
        <li>
            <nuxt-link to="/index.vue">Home page</nuxt-link>
        </li>
        <li>
            <nuxt-link to="/about">About</nuxt-link>
        </li>
    </ul>
</nav>
</header>
</template>
<template>
<nav class="flex flex-row gap-8 pr-4 text-8px text-green-200 font-family: 'script', apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;">
    <ul class="flex flex-row gap-4">
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/about" class="hover:text-orange-200 text-white text-sm">About</nuxt-link></li>
        <li><nuxt-link to="/contact" class="hover:text-orange-200 text-white text-sm">Contact</nuxt-link></li>
        <li><nuxt-link to="/blog" class="hover:text-orange-200 text-white text-sm">Blog</nuxt-link></li>
        <li><nuxt-link to="/projects" class="hover:text-orange-200 text-white text-sm">Projects</nuxt-link></li>
    </ul>
</nav>
</template>
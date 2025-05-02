<template>
    <div>
        <h1 class="text-4xl font-bold text-gray-900/80 border-gray-800/50 pb-4">{{ title }}</h1>
    </div>
</template>
<script setup>
const props = defineProps({
    title: String,
})
</script>
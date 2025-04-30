<template>
    <div>
        <h1 class="text-2xl border-b border-gray-200 pb-4">{{ title }}</h1>
    </div>
</template>
<script setup>
const props = defineProps({
    title: String,
})
</script>
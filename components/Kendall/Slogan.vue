<template>
    <div class="text-4xl"> {{ message }} </div>
</template>

<script setup>
defineProps({
    message: {
        default: "I really love HTML"
    }
});
</script>
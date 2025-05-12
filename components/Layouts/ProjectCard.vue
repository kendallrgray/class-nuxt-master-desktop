<template>
  <div
    class="bg-white rounded-lg shadow-md overflow-hidden transition-all duration-300"
    :class="{ 'hover:shadow-lg hover:scale-102': hoverEffect }"
  >
    <a :href="link" :target="target">
      <img :src="image" :alt="title" class="w-full h-48 object-cover" />
      <div class="p-4">
        <h3 class="font-bold text-gray-700 text-2xl">{{ title }}</h3>
        <p class="text-black p-4">{{ description }}</p>
        <div v-if="showReadMore" class="text-right">
          <span class="text-green-800 hover:text-green-900 font-medium">Read more →</span>
        </div>
      </div>
    </a>
  </div>
</template>

<script setup>
defineProps({
  image: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  link: {
    type: String,
    required: true
  },
  target: {
    type: String,
    default: "_blank"
  },
  showReadMore: {
    type: Boolean,
    default: false
  },
  hoverEffect: {
    type: Boolean,
    default: true
  }
});
</script>

<style scoped>
.hover\:scale-102:hover {
  transform: scale(1.02);
}
</style>

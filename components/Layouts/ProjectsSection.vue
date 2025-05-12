<template>
  <section class="py-8">
    <div v-if="title" class="mb-4">
      <PageHeader :title="title" :class="titleClass" />
      <p v-if="subtitle" class="text-lg text-gray-700/90 text-center">{{ subtitle }}</p>
    </div>
    
    <LayoutsProjectsGrid 
      :projects="projects" 
      :columns="columns"
      :showLoadMore="showLoadMore"
      :loadMoreText="loadMoreText"
      @load-more="$emit('load-more')"
    />
  </section>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    default: ''
  },
  subtitle: {
    type: String,
    default: ''
  },
  titleClass: {
    type: String,
    default: 'font-bold text-4xl text-gray-700 py-3'
  },
  projects: {
    type: Array,
    required: true
  },
  columns: {
    type: Number,
    default: 3
  },
  showLoadMore: {
    type: Boolean,
    default: false
  },
  loadMoreText: {
    type: String,
    default: 'Load More'
  }
});

defineEmits(['load-more']);
</script>

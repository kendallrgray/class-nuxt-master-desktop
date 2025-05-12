<template>
  <div>
    <div
      class="grid gap-8 mt-8"
      :class="[
        columns === 1 ? 'grid-cols-1' : '',
        columns === 2 ? 'grid-cols-1 sm:grid-cols-2' : '',
        columns === 3 ? 'grid-cols-1 sm:grid-cols-2 lg:grid-cols-3' : '',
        columns === 4 ? 'grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4' : ''
      ]"
    >
      <LayoutsProjectCard
        v-for="(project, index) in projects"
        :key="index"
        :image="project.image"
        :title="project.title"
        :description="project.description"
        :link="project.link"
        :target="project.target"
        :showReadMore="project.showReadMore"
        :hoverEffect="project.hoverEffect !== undefined ? project.hoverEffect : true"
      />
    </div>

    <!-- Show load more button if provided -->
    <div v-if="showLoadMore" class="flex justify-center mt-8">
      <button
        @click="$emit('load-more')"
        class="bg-green-800 hover:bg-green-900 text-white font-bold py-2 px-4 rounded"
      >
        {{ loadMoreText }}
      </button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  projects: {
    type: Array,
    required: true,
    default: () => []
  },
  columns: {
    type: Number,
    default: 3,
    validator: (value) => [1, 2, 3, 4].includes(value)
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

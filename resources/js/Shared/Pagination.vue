<template>
  <div data-component-name="pagination">
    <Component
      :is="link.url ? Link : 'span'"
      v-for="(link, index) in links"
      v-html="link.label"
      :key="index"
      :href="link.url"
      class="px-1"
      :class="{ 'font-bold': link.active, 'text-gray-500': !link.url }"
    />
  </div>
</template>

<script setup>
import { Link } from '@inertiajs/inertia-vue3'

defineProps({
  links: {
    type: Array,
    default: [],
  },
})
</script>

<template>
  <Link
    class="text-blue-600 hover:underline"
    :class="{ 'font-bold underline': active }"
  >
    <slot />
  </Link>
</template>

<script setup>
import { Link } from '@inertiajs/inertia-vue3'

defineProps({
  active: {
    type: Boolean,
    default: false,
  },
})
</script>

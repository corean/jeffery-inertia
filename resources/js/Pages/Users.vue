<template>
  <h1 class="mb-4">Users</h1>
  <Nav />

  <div style="margin-top: 1000px">
    <p>current time is {{ time }}</p>
    <Link href="/users" class="text-blue-500" preserve-scroll>Refresh</Link>
  </div>
</template>

<script setup>
import Nav from '@/Shared/Nav.vue'
import { Link } from '@inertiajs/inertia-vue3'
defineProps({
  time: String,
})
</script>

<style scoped></style>

<template>
  <div class="bg-gray-200 p-6">
    <header class="align-items-center flex justify-between">
      <div class="flex items-center">
        <h1 class="text-lg font-bold">My App</h1>
        <input type="text" value="11" />
        <p class="ml-2 text-sm">Welcome to, {{ username }}</p>
      </div>
      <Nav />
    </header>
  </div>
  <section class="p-6">
    <div class="mx-auto max-w-3xl">
      <slot></slot>
    </div>
  </section>
</template>

<script setup>
import Nav from '@/Shared/Nav.vue'
import { computed } from 'vue'
import { usePage } from '@inertiajs/inertia-vue3'

const username = computed(() => usePage().props.value.auth.user.username)
</script>

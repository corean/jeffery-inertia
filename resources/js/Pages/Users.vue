<template>
  <Head>
    <meta
      name="description"
      content="My App User Page"
      head-key="description"
    />
  </Head>
  <h1 class="text-2xl">Users</h1>

  <ul>
    <li v-for="user in users" key="user.id" v-html="user.name"></li>
  </ul>
</template>

<script setup>
import { Head } from '@inertiajs/inertia-vue3'
defineProps({
  users: {
    type: Array,
    default: [],
  },
})
</script>

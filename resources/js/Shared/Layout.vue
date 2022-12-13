<template>
  <div class="bg-gray-200 p-6">
    <header class="align-items-center flex justify-between">
      <h1 class="text-lg font-bold">My App</h1>
      <Nav />
    </header>
  </div>
  <section class="p-6">
    <div class="mx-auto max-w-3xl">
      <slot></slot>
    </div>
  </section>
</template>

<script>
import Nav from '@/Shared/Nav.vue'

export default {
  name: 'Layout',
  components: { Nav },
}
</script>

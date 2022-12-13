<template>
  <nav>
    <ul class="list-disc">
      <li>
        <NavLink href="/" :active="$page.component === 'Home'">Home</NavLink>
      </li>
      <li>
        <NavLink href="/users" :active="$page.component === 'Users'"
          >Users</NavLink
        >
      </li>
      <li>
        <NavLink href="/settings" :active="$page.component === 'Settings'"
          >Settings</NavLink
        >
      </li>
      <li>
        <Link
          href="/logout"
          class="text-blue-600 hover:underline"
          method="post"
          as="button"
          >logout
        </Link>
      </li>
    </ul>
  </nav>
</template>

<script setup>
import { Link } from '@inertiajs/inertia-vue3'
import NavLink from '@/Shared/NavLink.vue'
</script>

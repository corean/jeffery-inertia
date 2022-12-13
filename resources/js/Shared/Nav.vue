<template>
  <nav>
    <ul class="list-disc">
      <li>
        <Link href="/" class="text-blue-600 hover:underline">Home </Link>
      </li>
      <li>
        <Link href="/users" class="text-blue-600 hover:underline">Users </Link>
      </li>
      <li>
        <Link href="/settings" class="text-blue-600 hover:underline"
          >Settings
        </Link>
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
</script>

<template>
  <Head>
    <meta
      name="description"
      content="My App User Page"
      head-key="description"
    />
  </Head>
  <h1 class="text-2xl">Users</h1>
  <!--
  <ul>
    <li v-for="user in users" :key="user.id" v-html="user.name" />
  </ul>
  -->

  <div class="flex flex-col">
    <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
      <div class="inline-block min-w-full py-2 align-middle sm:px-6 lg:px-8">
        <div
          class="overflow-hidden border-b border-gray-200 shadow sm:rounded-lg"
        >
          <table class="min-w-full divide-y divide-gray-200">
            <tbody class="divide-y divide-gray-200 bg-white">
              <tr v-for="user in users " :key="user.id">
                <td class="whitespace-nowrap px-6 py-4">
                  <div class="flex items-center">
                    <div>
                      <div class="text-sm font-medium text-gray-900">
                        {{ user.name }}
                      </div>
                    </div>
                  </div>
                </td>

                <td
                  class="whitespace-nowrap px-6 py-4 text-right text-sm font-medium"
                >
                  <Link
                    :href="`/users/${user.id}/edit`"
                    class="text-indigo-600 hover:text-indigo-900"
                  >
                    Edit
                  </Link>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Head, Link } from '@inertiajs/inertia-vue3'

defineProps({
  users: {
    type: Array,
    default: [],
  },
})
</script>

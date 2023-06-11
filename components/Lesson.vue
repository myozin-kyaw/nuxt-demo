<template>
  <div
    class="relative flex items-center space-x-3 rounded-lg border border-gray-300 bg-white px-6 py-5 shadow-sm focus-within:ring-2 focus-within:ring-emerald-500 focus-within:ring-offset-2 hover:border-emerald-400"
    :class="{'border-gray-700 border-1 bg-slate-200 hover:border-gray-800 focus-within:ring-gray-700' : disabled}"
  >
    <div class="flex-shrink-0">
      <slot/>
      <!-- <img class="h-10 w-10 rounded-full" :src="person.imageUrl" alt="" /> -->
    </div>
    <NuxtLink v-if="!disabled" :to="to" class="min-w-0 flex-1">
      <span class="absolute inset-0" aria-hidden="true" />
      <p class="text-sm font-medium text-gray-900">{{ name }}</p>
    </NuxtLink>
    <div v-else class="min-w-0 flex-1">
      <span class="absolute inset-0" aria-hidden="true" />
      <p class="text-sm font-medium text-gray-900">{{ name }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  name: {
    type: String,
    default: null
  },
  to: {
    type: String,
    default: '#'
  },
  disabled: {
    type: Boolean,
    default: false
  }
});
</script>
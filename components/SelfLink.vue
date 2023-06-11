<template>
    <NuxtLink :to="to" class="text-emerald-400 underline">
        {{ name }}
    </NuxtLink>
</template>

<script setup> 
defineProps(['name', 'href'])
</script>
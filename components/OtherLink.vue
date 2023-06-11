<template>
    <a :href="href" target="__blank" class="text-emerald-400 underline">
        {{ name }}
    </a>
</template>

<script setup> 
defineProps(['name', 'href'])
</script>
<template>
  <button
    class="bg-gradient-to-r from-primary to-secondary text-white px-10 py-3 rounded-lg font-semibold hover:opacity-85 primary-light transition-all duration-500 ease-in-out"
  >
    <p class="text-xl">{{ label }}</p>
    <p class="font-[300] text-sm leading-4">{{ description }}</p>
  </button>
</template>

<script setup lang="ts">
defineProps<{
  label: string;
  description: string;
}>();
</script>

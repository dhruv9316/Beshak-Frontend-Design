<template>
  <div
    class="flex flex-col items-center text-center px-4 sm:px-8 py-4 sm:py-8 bg-secondary-light sm:bg-transparent rounded-xl mr-4 sm:mr-0"
  >
    <img :src="icon" :alt="label" class="w-8 h-8 mb-4" loading="lazy" />

    <h3 class="text-sm sm:text-xl font-bold leading-tight text-[#18181B] mb-2">
      {{ label }}
    </h3>
    <p class="text-xs sm:text-base text-[#3F3F46] font-medium">
      {{ description }}
    </p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  icon: string;
  label: string;
  description: string;
}>();
</script>

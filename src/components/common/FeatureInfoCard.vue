<template>
  <div
    class="flex w-full min-w-0 flex-col items-center text-center px-4 sm:px-8 py-4 sm:py-8 bg-secondary-light sm:bg-transparent rounded-xl sm:w-auto"
    :class="{ 'h-full min-h-0': fillHeight }"
  >
    <img
      :src="icon"
      :alt="label"
      class="w-8 h-8 mb-4 shrink-0"
      loading="lazy"
    />

    <h3
      class="text-sm sm:text-xl font-bold leading-tight text-[#18181B] mb-2 shrink-0"
    >
      {{ label }}
    </h3>
    <p class="text-xs sm:text-base text-[#3F3F46] font-medium shrink-0">
      {{ description }}
    </p>
    <div v-if="fillHeight" class="min-h-0 flex-1" aria-hidden="true" />
  </div>
</template>

<script setup lang="ts">
defineProps<{
  icon: string;
  label: string;
  description: string;
  fillHeight?: boolean;
}>();
</script>

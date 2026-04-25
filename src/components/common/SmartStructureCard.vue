<template>
  <div
    class="w-full flex flex-row sm:flex-col gap-6 sm:gap-0 items-start sm:items-center text-center bg-white rounded-md px-8 py-10 shadow-xl hover:shadow-2xl transition-shadow duration-300"
  >
    <img :src="icon" :alt="label" class="w-10 h-10 mb-6" loading="lazy" />

    <div class="flex flex-col items-start sm:items-center justify-start">
      <h3
        class="text-xl sm:text-2xl font-bold leading-tight text-[#18181B] mb-3"
      >
        {{ label }}
      </h3>
      <p class="text-sm sm:text-base font-medium text-[#181818] text-left">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  icon: string;
  label: string;
  description: string;
}>();
</script>

<template>
  <div
    class="w-full flex flex-col items-center text-center bg-white rounded-md px-8 py-10 shadow-xl hover:shadow-2xl transition-shadow duration-300"
  >
    <img :src="icon" :alt="label" class="w-10 h-10 mb-6" loading="lazy" />

    <h3 class="text-[32px] font-semibold leading-tight text-[#18181B] mb-3">
      {{ label }}
    </h3>
    <p class="text-base font-medium text-[#181818]">
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

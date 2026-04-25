<template>
  <div class="flex flex-col shadow-lg w-32 sm:w-44">
    <div
      :class="[
        'flex justify-center rounded-tl-xl rounded-tr-xl p-2 sm:p-4 text-center text-white',
        variant === 'primary'
          ? 'bg-gradient-to-r from-primary to-primary-light'
          : 'bg-gradient-to-r from-[#52525B] to-[#A1A1AA]',
      ]"
    >
      <div class="flex flex-col gap-1">
        <p
          class="text-xl sm:text-5xl font-extrabold flex items-start justify-center gap-1"
        >
          {{ rate }}
        </p>

        <p class="text-xs sm:text-base leading-4 font-medium">
          {{ variant === "primary" ? "(TAX FREE)" : "(AFTER TAX)" }}
        </p>
      </div>

      <p class="text-sm">*</p>
    </div>

    <div
      :class="[
        'rounded-bl-xl rounded-br-xl p-2 sm:p-4 text-center bg-white font-semibold text-xs sm:text-base leading-4',
        variant === 'primary' ? 'text-secondary' : 'text-[#71717A]',
      ]"
    >
      {{ label }}
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  rate: string;
  label: string;
  variant: "primary" | "secondary";
}>();
</script>

<template>
  <div
    class="bg-white rounded-md shadow-sm w-full hover:shadow-2xl transition-shadow duration-300"
  >
    <div class="px-4 pt-5 pb-4 flex flex-col items-center gap-4">
      <div class="bg-[#F4F4F5] rounded-sm px-3 py-2">
        <img
          src="../../assets/images/hdfc-life-logo.png"
          :alt="tenure"
          class="h-7 object-contain"
          loading="lazy"
        />
      </div>

      <p class="text-base font-bold text-[#18181B]">HDFC Life</p>
      <p class="text-base text-[#3F3F46] -mt-2">Sanchay Plus</p>
      <p class="text-5xl font-bold leading-none text-primary mb-1">
        {{ rate }}
      </p>
      <p class="text-sm text-[#3F3F46] -mt-2">Guaranteed return p.a.</p>

      <div
        class="flex items-center gap-2 rounded-full bg-secondary-light px-3 py-1"
      >
        <img
          src="../../assets/icons/percentage.svg"
          alt="percentage"
          class="w-3 h-3"
        />
        <span class="text-[11px] font-semibold text-primary">
          TAX-FREE U/S 10(10D)
        </span>
      </div>
    </div>

    <div class="h-px bg-[#D4D4D8] w-[90%] mx-auto" />

    <div class="px-4 py-3 flex items-start justify-between">
      <div>
        <p class="text-base leading-4 font-bold text-[#18181B]">{{ tenure }}</p>
        <p class="text-xs text-[#52525B]">lock-in period</p>
      </div>

      <div class="text-right">
        <p class="text-base leading-4 font-bold text-[#18181B]">{{ amount }}</p>
        <p class="text-xs text-[#52525B]">min/year</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  rate: string;
  tenure: string;
  amount: string;
}>();
</script>

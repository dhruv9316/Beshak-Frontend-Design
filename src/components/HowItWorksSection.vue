<template>
  <section class="px-6 sm:px-24 py-4 sm:py-16 my-10">
    <div class="mx-auto">
      <h2
        class="text-center text-2xl sm:text-5xl font-bold text-[#18181B] mb-12"
      >
        How it works. 3 simple steps
      </h2>

      <div class="hidden md:flex items-center justify-center mb-10">
        <div
          v-for="(step, index) in steps"
          :key="`step-number-${step.number}`"
          class="flex items-center"
        >
          <span class="text-secondary text-5xl font-medium">{{
            step.number
          }}</span>

          <span
            v-if="index !== steps.length - 1"
            class="block w-36 lg:w-[320px] border-t-2 border-dashed border-[#A1A1AA] mx-8"
            aria-hidden="true"
          />
        </div>
      </div>

      <div class="flex flex-col md:flex-row gap-8 md:gap-10 text-[#18181B]">
        <div
          v-for="(step, index) in steps"
          :key="step.number"
          class="flex-1 text-center"
        >
          <p class="md:hidden text-secondary text-4xl font-medium mb-4">
            {{ step.number }}
          </p>
          <h3 class="text-2xl font-bold leading-tight mb-3">
            {{ step.label }}
          </h3>
          <p class="text-base max-w-[80%] mx-auto">
            {{ step.description }}
          </p>

          <p
            v-if="index !== steps.length - 1"
            class="sm:hidden h-12 w-1 border-r-2 border-dashed border-[#A1A1AA] mx-auto mt-6"
          ></p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const steps = [
  {
    number: "01",
    label: "We connect you to an Expert",
    description:
      "You consult with a professional life insurance expert with 5+ yrs of experience",
  },
  {
    number: "02",
    label: "Expert understands your needs",
    description:
      "Expert understands you, your long term financial goals, your current investments.",
  },
  {
    number: "03",
    label: "Find suitable plans, if any",
    description:
      "Expert shortlists suitable plans per your needs. Helps you buy it right",
  },
];
</script>

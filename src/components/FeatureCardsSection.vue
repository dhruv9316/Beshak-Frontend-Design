<template>
  <section class="flex flex-col items-center bg-white px-4 sm:px-24 py-10">
    <p class="sm:hidden mb-8 text-2xl leading-7 font-bold mx-auto">
      Why trust Beshak?
    </p>

    <div
      class="flex flex-row overflow-x-scroll no-scrollbar gap-2 items-center sm:gap-0 w-full"
    >
      <div
        v-for="(card, index) in featureCards"
        :key="card.label"
        class="relative flex-1"
      >
        <FeatureInfoCard
          :icon="card.icon"
          :label="card.label"
          :description="card.description"
        />
        <span
          v-if="index !== featureCards.length - 1"
          class="hidden lg:block absolute right-0 top-1/2 -translate-y-1/2 h-20 w-px bg-[#D4D4D8]"
          aria-hidden="true"
        />
      </div>
    </div>

    <div class="flex sm:hidden justify-center gap-2 mt-6">
      <span
        class="h-1 rounded-full transition-all duration-300 w-6 bg-[#2E9B52]"
      />
      <span
        class="h-1 rounded-full transition-all duration-300 w-6 bg-[#D4D4D8]"
      />
      <span
        class="h-1 rounded-full transition-all duration-300 w-6 bg-[#D4D4D8]"
      />
    </div>
  </section>
</template>

<script setup lang="ts">
import FeatureInfoCard from "./common/FeatureInfoCard.vue";
import balanceScaleIcon from "../assets/icons/balance-scale.svg";
import hatIcon from "../assets/icons/hat.svg";
import notAllowedIcon from "../assets/icons/not-allowed.svg";
import smilyIcon from "../assets/icons/smily.svg";

const featureCards = [
  {
    icon: balanceScaleIcon,
    label: "India's only 100% Unbiased platform",
    description: "No ads/commissions from insurers",
  },
  {
    icon: hatIcon,
    label: "Guidance from Real Experts",
    description: "Not salesmen. Not call centre agents",
  },
  {
    icon: notAllowedIcon,
    label: "Zero Charge. Zero Spam",
    description: "Pay nothing for the Consultation",
  },
  {
    icon: smilyIcon,
    label: "32K+ Happy Users",
    description: "Since 2020",
  },
];
</script>

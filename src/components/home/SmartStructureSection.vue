<template>
  <section class="px-4 sm:px-24 py-16">
    <h2
      class="text-center text-2xl sm:text-5xl font-bold text-[#18181B] mb-6 sm:mb-12"
    >
      Not just better returns. A smarter structure.
    </h2>

    <div class="flex flex-wrap -mx-3 -my-3">
      <div
        v-for="card in cards"
        :key="card.label"
        class="w-full md:w-1/2 lg:w-1/3 px-3 py-3 flex"
      >
        <SmartStructureCard
          :icon="card.icon"
          :label="card.label"
          :description="card.description"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import SmartStructureCard from "../common/SmartStructureCard.vue";
import stockUpIcon from "../../assets/icons/stock-up.svg";
import shieldIcon from "../../assets/icons/shield.svg";
import searchingIcon from "../../assets/icons/searching.svg";
import umbrellaIcon from "../../assets/icons/umbrella.svg";
import taxFreeIcon from "../../assets/icons/tax-free.svg";
import flexibleDatesIcon from "../../assets/icons/flexible-dates.svg";

const cards = [
  {
    icon: stockUpIcon,
    label: "Guaranteed Returns",
    description:
      "Up to 6.9% p.a. Not market-linked. Not dependent on fund performance. Your rate is locked from the day you invest.",
  },
  {
    icon: shieldIcon,
    label: "Locked in for 10-15 years",
    description:
      "Your future self will thank you for not touching this money. The rate stays the same, even if FD rates drop next year.",
  },
  {
    icon: searchingIcon,
    label: "Curated, Not Dumped",
    description:
      "Every plan here cleared our review. We looked at 40+ GSPs and rejected more than we picked.",
  },
  {
    icon: umbrellaIcon,
    label: "Life Cover Included",
    description:
      "Each plan includes a basic life cover, up to 10x the annual premium. Not a replacement for term insurance, but adds a level of protection.",
  },
  {
    icon: taxFreeIcon,
    label: "Tax-Free Returns",
    description:
      "Your maturity amount is tax free, so you receive the full payout. No deductions, unlike with fixed deposits.",
  },
  {
    icon: flexibleDatesIcon,
    label: "Flexible Payment Plans",
    description:
      "Choose from monthly, half-yearly, yearly, or one-time payments, with policy terms aligned to your goals.",
  },
];
</script>

<template>
  <section
    class="bg-gradient-to-b from-white to-[#E0F8E8] px-6 md:px-10 lg:px-24 pt-10 sm:pt-24 pb-0 sm:pb-10 xl:pb-0 overflow-hidden"
  >
    <div
      class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-10"
    >
      <div
        class="flex flex-col gap-6 sm:gap-8 text-center sm:text-left items-center sm:items-start flex-1"
      >
        <p class="text-[#7C3AED] font-bold text-sm sm:text-base">
          GUARANTEED SAVINGS PLANS
        </p>

        <h1 class="text-4xl md:text-6xl font-bold leading-tight">
          Earn more than FDs.<br />
          <span
            class="bg-gradient-to-r from-[#227340] to-[#33AB5F] text-transparent bg-clip-text"
          >
            Guaranteed!
          </span>
        </h1>

        <p class="text-base sm:text-lg font-medium text-[#181818] max-w-md">
          Life insurance plans with excellent returns from India's Top Insurers.
          100% Tax Free. Consult an Expert & understand whether it fits your
          needs.
        </p>

        <div
          class="flex flex-col md:flex-row items-center gap-4 md:gap-8 w-full md:w-auto"
        >
          <GradientButton
            label="Talk to an Expert"
            description="Honest Advice. No charge. No spam!"
            class="w-full sm:w-auto text-center"
          />
          <RatingBadge />
        </div>
      </div>

      <div class="relative flex justify-center flex-1 mt-16 sm:mt-0">
        <!-- Person Image -->
        <img
          src="../../assets/images/hero-image.png"
          alt="person"
          class="w-[280px] sm:w-[520px] object-contain relative z-10"
          loading="lazy"
        />

        <!-- Absolute Cards -->
        <div
          class="absolute -top-12 -left-2 md:-top-[74px] md:-left-4 xl:-top-16 xl:left-5 z-20"
        >
          <InterestCard
            rate="6.1%"
            label="Guarantee Savings Plans"
            variant="primary"
          />
        </div>
        <div
          class="absolute bottom-20 -right-3 md:bottom-36 md:-right-6 xl:bottom-56 xl:right-4 z-20"
        >
          <InterestCard rate="4.6%" label="Fixed Deposit" variant="secondary" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import RatingBadge from "../RatingBadge.vue";
import GradientButton from "../common/GradientButton.vue";
import InterestCard from "../common/InterestCard.vue";
</script>

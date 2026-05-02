<template>
  <section class="flex flex-col items-center bg-white px-4 py-10 lg:px-24">
    <p class="mb-8 text-center text-2xl font-bold leading-7 sm:hidden">
      Why trust Beshak?
    </p>

    <div class="feature-swiper w-full max-w-full lg:hidden">
      <Swiper
        :modules="[Pagination, Autoplay]"
        :slides-per-view="2"
        :space-between="8"
        :pagination="{ clickable: true }"
        :autoplay="{
          delay: 2000,
          disableOnInteraction: false,
          pauseOnMouseEnter: true,
        }"
        :watch-overflow="true"
        :breakpoints="{ 450: { slidesPerView: 3 } }"
        class="!pb-0"
        role="region"
        aria-label="Why trust Beshak"
      >
        <SwiperSlide
          v-for="card in featureCards"
          :key="card.label"
          class="feature-slide"
        >
          <FeatureInfoCard
            :icon="card.icon"
            :label="card.label"
            :description="card.description"
            fill-height
          />
        </SwiperSlide>
      </Swiper>
    </div>

    <div
      class="hidden lg:flex w-full max-w-full flex-nowrap items-stretch"
      role="region"
    >
      <div
        v-for="(card, index) in featureCards"
        :key="card.label"
        class="relative min-w-0 flex-1"
      >
        <FeatureInfoCard
          :icon="card.icon"
          :label="card.label"
          :description="card.description"
          fill-height
        />
        <span
          v-if="index !== featureCards.length - 1"
          class="absolute right-0 top-1/2 hidden h-28 w-px -translate-y-1/2 bg-[#D4D4D8] lg:block"
          aria-hidden="true"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";
import FeatureInfoCard from "./../common/FeatureInfoCard.vue";
import balanceScaleIcon from "../../assets/icons/balance-scale.svg";
import hatIcon from "../../assets/icons/hat.svg";
import notAllowedIcon from "../../assets/icons/not-allowed.svg";
import smilyIcon from "../../assets/icons/smily.svg";

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

<style scoped>
.feature-swiper :deep(.swiper-wrapper) {
  align-items: stretch;
}

.feature-swiper :deep(.feature-slide) {
  display: flex;
  height: auto;
}

.feature-swiper :deep(.feature-slide) > * {
  flex: 1 1 0;
  min-width: 0;
}

.feature-swiper :deep(.swiper-pagination) {
  position: static;
  margin-top: 1.5rem;
  transform: none;
}

.feature-swiper :deep(.swiper-pagination-bullet) {
  width: 1.5rem;
  height: 0.25rem;
  border-radius: 9999px;
  opacity: 1;
  background-color: #d4d4d8;
  margin: 0 0.25rem;
  transition:
    background-color 0.3s,
    width 0.3s;
}

.feature-swiper :deep(.swiper-pagination-bullet-active) {
  width: 1.5rem;
  background-color: #33ab5f;
}
</style>

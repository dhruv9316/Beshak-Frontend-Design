<template>
  <section
    class="bg-gradient-to-r from-primary to-primary-light px-6 lg:px-24 py-4 lg:py-16"
  >
    <div class="max-w-[1400px] mx-auto">
      <h2
        class="text-center text-2xl sm:text-3xl lg:text-5xl font-bold text-white mb-4"
      >
        Carefully Verified Plans. Experts Recommend.
      </h2>
      <p
        class="text-center text-sm sm:text-lg lg:text-xl text-[#ECFDF3] lg:max-w-[50%] mx-auto mb-12"
      >
        Out of 40+ plans reviewed only 4 made the cut. Every figure is real,
        post-tax, and independently verified. No inflated projections.
      </p>

      <div class="feature-swiper w-full max-w-full">
        <Swiper
          :modules="[Pagination, Autoplay]"
          :slides-per-view="1"
          :space-between="8"
          :pagination="{ clickable: true }"
          :autoplay="{
            delay: 2000,
            disableOnInteraction: false,
            pauseOnMouseEnter: true,
          }"
          :watch-overflow="true"
          :breakpoints="{
            640: { slidesPerView: 2 },
            768: { slidesPerView: 3 },
            1024: { slidesPerView: 4 },
          }"
          class="!pb-0"
          role="region"
          aria-label="Why trust Beshak"
        >
          <SwiperSlide
            v-for="plan in plans"
            :key="`${plan.rate}-${plan.amount}`"
            class="feature-slide"
          >
            <VerifiedPlanCard
              :rate="plan.rate"
              :tenure="plan.tenure"
              :amount="plan.amount"
            />
          </SwiperSlide>
        </Swiper>
      </div>

      <p
        class="text-center text-white text-base sm:text-lg leading-5 font-bold my-8"
      >
        Don’t buy these plans yet!<br class="hidden sm:block" />
        Talk to an Expert who will evaluate it for you in detail!
      </p>

      <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
        <button
          type="button"
          class="w-full sm:w-fit inline-flex items-center justify-center gap-2 bg-white text-[#18181B] font-semibold rounded-md px-8 py-3 border border-white min-w-56 hover:scale-105 transition-all duration-500"
        >
          <img
            src="../../assets/icons/video-recorder.svg"
            alt=""
            class="w-5 h-5"
            aria-hidden="true"
          />
          <span>Talk to an Expert</span>
        </button>

        <button
          type="button"
          class="w-full sm:w-fit inline-flex items-center justify-center gap-2 bg-transparent text-white font-semibold rounded-md px-8 py-3 border border-secondary-light min-w-56 hover:scale-105 transition-all duration-500"
        >
          <img
            src="../../assets/icons/whatsapp.svg"
            alt=""
            class="w-5 h-5"
            aria-hidden="true"
          />
          <span>Chat with Us</span>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import VerifiedPlanCard from "../common/VerifiedPlanCard.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

const plans = [
  {
    rate: "6.2%",
    tenure: "15 year",
    amount: "₹1,00,000",
  },
  {
    rate: "6.0%",
    tenure: "12 year",
    amount: "₹75,000",
  },
  {
    rate: "5.9%",
    tenure: "10 year",
    amount: "₹50,000",
  },
  {
    rate: "5.8%",
    tenure: "10 year",
    amount: "₹25,000",
  },
];
</script>

<style scoped>
.feature-swiper :deep(.swiper-pagination) {
  position: static;
  margin-top: 1rem;
  transform: none;
}

.feature-swiper :deep(.swiper-pagination-bullet) {
  width: 1.5rem;
  height: 0.25rem;
  border-radius: 9999px;
  opacity: 1;
  background-color: #1e8a46;
  margin: 0 0.25rem;
  transition:
    background-color 0.3s,
    width 0.3s;
}

.feature-swiper :deep(.swiper-pagination-bullet-active) {
  width: 1.5rem;
  background-color: #fff;
}
</style>

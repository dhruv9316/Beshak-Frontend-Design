<template>
  <section
    class="bg-[#E0F8E8] px-6 sm:px-24 py-4 sm:py-14 sm:max-w-[90%] mx-auto flex flex-col gap-16 my-10 rounded-xl items-center"
  >
    <div
      class="flex flex-col sm:flex-row gap-10 lg:gap-16 items-center sm:justify-between"
    >
      <div class="flex-1 flex flex-col items-center sm:items-start">
        <h2
          class="text-2xl sm:text-[40px] leading-[48px] font-bold text-[#18181B] mb-4"
        >
          Build stability as you grow
        </h2>
        <p
          class="text-secondary text-lg sm:text-xl font-semibold sm:max-w-[70%] mb-6 text-center sm:text-left"
        >
          Assuming you're 30. Roughly 30% of your money should be in something
          stable.
        </p>

        <p
          class="text-base text-[#18181B] sm:max-w-[75%] font-medium text-center sm:text-left"
        >
          You're probably heavy on equity. Mutual funds, stocks, maybe some
          crypto. That's fine for growth. But your portfolio needs a stable base
          too. A general rule: invest a percentage equal to your age in low-risk
          instruments. Guaranteed Savings Plans fit that slot perfectly. Not
          instead of your SIPs. Alongside them.
        </p>
      </div>

      <div class="h-[300px] sm:h-[360px] aspect-square">
        <PieChart />
      </div>
    </div>

    <div
      class="flex flex-col-reverse sm:flex-row gap-10 lg:gap-16 items-center"
    >
      <div class="flex flex-col items-center justify-center">
        <div
          class="rounded-xl bg-gradient-to-r from-primary to-primary-light text-white shadow-xl px-12 py-6 mb-5 flex flex-col items-center max-w-fit"
        >
          <p class="text-base tracking-wide font-semibold">ONLY</p>
          <p class="text-[44px] leading-[48px] font-bold my-2">4</p>
          <p class="text-sm font-semibold">MADE THE CUT</p>
        </div>

        <div class="flex gap-4">
          <div
            class="bg-white rounded-xl shadow-xl px-14 py-7 text-center min-w-[170px] text-sm font-semibold text-[#18181B]"
          >
            <p class="text-3xl font-bold">40+</p>
            <p class="mt-2">PLANS</p>
            <p>REVIEWED</p>
          </div>

          <div
            class="bg-white rounded-xl shadow-xl px-12 py-7 text-center min-w-[170px] text-sm font-semibold text-[#18181B]"
          >
            <p class="text-3xl font-bold">0</p>
            <p class="mt-2">INFLATED</p>
            <p>PROJECTIONS</p>
          </div>
        </div>
      </div>

      <div class="flex-1 flex flex-col items-center sm:items-start">
        <h3
          class="text-2xl sm:text-[40px] leading-[48px] font-bold text-[#18181B] mb-4"
        >
          Handpicked, not hard sold
        </h3>
        <p
          class="text-secondary text-lg sm:text-xl font-semibold sm:max-w-[70%] mb-6 text-center sm:text-left"
        >
          We know Guaranteed Savings Plans get mis-sold. That's exactly why we
          built this.
        </p>

        <p
          class="text-base text-[#18181B] max-w-[95%] font-medium text-center sm:text-left"
        >
          Insurance agents routinely push Guaranteed Savings Plans with inflated
          return projections and buried lock-ins. We've seen it for years. Every
          plan here was reviewed by our team for real, post-tax returns, no IRR
          manipulation, no plans designed for the distributor's benefit over
          yours. That's the Beshak standard.
        </p>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import PieChart from "./common/PieChart.vue";
</script>

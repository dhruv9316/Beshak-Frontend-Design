<template>
  <div class="flex items-center gap-3 text-sm text-gray-600">
    <img src="../assets/icons/google.svg" class="w-8" />

    <div class="flex flex-col text-[#181818]">
      <div class="text-base font-bold flex items-center gap-1">
        <p>4.9</p>

        <p class="flex items-center">
          <img v-for="_ in 4" src="../assets/icons/star-full.svg" alt="star" />
          <img src="../assets/icons/star-partial.svg" alt="star-partial" />
        </p>
      </div>
      <p class="text-xs font-normal">Rating on google</p>
    </div>
  </div>
</template>

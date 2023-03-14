<template>
  <div class="flexCenter w-[140px] h-[140px] rounded-full bg-blue-gradient p-[2px] cursor-pointer">
    <div class="flexCenter flex-col bg-black w-[100%] h-[100%] rounded-full">
      <div class="flexStart flex-row">
        <p class="font-poppins font-medium text-[18px] leading-[23px] mr-2">
          <span class="text-gradient">Get</span>
        </p>
        <img :src="arrowUp" class="w-[23px] h-[23px] object-contain" alt="">
      </div>
      <p class="font-poppins font-medium text-[18px] leading-[23px]">
        <span class="text-gradient">Started</span>
      </p>
    </div>
  </div>
</template>

<script setup>
import { arrowUp } from '~~/assets';
</script>

<style lang="scss" scoped></style>
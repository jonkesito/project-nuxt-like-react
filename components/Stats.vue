<template>
  <section class="flexCenter flex-row px-10 flex-wrap sm:mb-20 mb-6">
    <div class="flex-1 flex justify-start  items-center flex-row m-3" v-for="item in stats" :key="item.id">
      <h4
        class="font-poppins font-semibold xs:text-[40.89px] text-[30.89px] xs:leading-[53.16px] leading-[43.16px] text-white">
        {{ item.value }}
      </h4>
      <p
        class="font-poppins font-normal xs:text-[20.45px] text-[15.45px] xs:leading-[26.58px] leading-[21.58px] text-gradient uppercase ml-3">
        {{ item.title }}
      </p>
    </div>
  </section>
</template>

<script setup>
import { stats } from '~~/constants';
</script>

<style lang="scss" scoped></style>
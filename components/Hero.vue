<script setup>
import { discount, robot } from '~~/assets';
</script>

<template>
  <section id="home" class="flex md:flex-row flex-col paddingY paddingX">
    <div class="flex-1 flexStart flex-col xl:px-0 sm:px-16 px-6">
      <div class="flex flex-row items-center py-[6px] px-4 bg-discount-gradient rounded-[10px] mb-2">
        <img :src="discount" alt="discount" class="w-[32px] h-[32px]">
        <p class="paragraph ml-5">
          <span>20%</span>
          discount for
          <span>1 Month</span>
          {{ " " }}
          <span>Account</span>
        </p>
      </div>

      <div class="flex mt-5 flex-row justify-between gap-8 items-center w-full">
        <h1
          class="flex-1 font-poppins font-semibold ss:text-[68px] text-[52px] text-white ss:leading-[100.8px] leading-[75px]">
          The Next <br class="sm:block hidden">{{ " " }}
          <span class="text-gradient font-bold">Generation</span>
        </h1>

        <div class="ss:flex hidden md:mr-4 mr-0">
          <GetStarted />
        </div>
      </div>

      <h1
        class="font-poppins font-semibold ss:text-[60px] text-[52px] text-white ss:leading-[100.8px] leading-[75px] w-full">
        Payment Method.
      </h1>

      <p class="paragraph  max-w-[470px] mt-5" }>
        Our team of experts uses a methodology to identify the credit cards
        most likely to fit your needs. We examine annual percentage rates,
        annual fees.
      </p>
    </div>
    <picture class="flex-1 flex flexCenter md:my-0 my-10 relative">
      <img :src="robot" alt="" class="w-[100%] h-[100%] relative z-[5]">
      <div class="absolute z-[0] w-[40%] h-[35%] top-0 pink__gradient" />
      <div class="absolute z-[1] w-[80%] h-[80%] rounded-full white__gradient bottom-40" />
      <div class="absolute z-[0] w-[50%] h-[50%] right-20 bottom-20 blue__gradient" />
    </picture>

    <div class="ss:hidden flexCenter"></div>
  </section>
</template>

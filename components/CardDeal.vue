<template>
  <section class="section">
    <div class="sectionInfo">
      <h2 class="heading2">
        Find a better card deal <br class="sm:block hidden" /> in few easy
        steps.
      </h2>
      <p class="paragraph max-w-[470px] mt-5">
        Arcu tortor, purus in mattis at sed integer faucibus. Aliquet quis
        aliquet eget mauris tortor.ç Aliquet ultrices ac, ametau.
      </p>

      <Button styles="mt-10" />
    </div>

    <div class="sectionImg">
      <img :src="card" alt="billing" class="w-[100%] h-[100%]">
    </div>
  </section>
</template>

<script setup>
import Button from './Button.vue';
import { card } from '~~/assets';
</script>

<style lang="scss" scoped></style>
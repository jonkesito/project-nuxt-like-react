<script setup>
import { features } from '~~/constants';
import Button from './Button.vue';
</script>

<template>
  <section id="features" class="section">
    <div class="sectionInfo">
      <h2 class="heading2">You do the business,<br class="sm:block hidden" /> we'll handle the money.</h2>
      <p class="paragraph max-w-[470px] mt-5">With the right credit card, you can improve your financial life by
        building credit, earning rewards and saving money. But with hundreds
        of credit cards on the market.</p>
      <Button styles="mt-10" />
    </div>

    <div class="sectionImg flex-col">
      <FeatureCard v-for="(feature, index) in features" :key="feature.id" :feature="feature" :index="index" />
    </div>
  </section>
</template>


<style lang="scss" scoped></style>
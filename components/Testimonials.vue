<script setup>
import { feedback } from '~~/constants'; 
</script>

<template>
  <section id="client" class="paddingY flexCenter flex-col relative">
    <div class="w-full flex justify-between items-center md:flex-row flex-col sm:mb-16 mb-6 relative z-[1]">
      <h2 class="heading2">
        What People are <br class="sm:block hidden" /> saying about us
      </h2>
      <div class="w-full md:mt-0 mt-6">
        <p class="paragragh text-left max-w-[450px]">
          Everything you need to accept card payments and grow your business
          anywhere on the planet.
        </p>
      </div>
    </div>

    <div class="flex flex-wrap sm:justify-start justify-center w-full feedback-container relative z-[1]">
      <Feedback v-for="(card, index) in feedback" :key="index" :feedback="card" />
    </div>
  </section>
</template>


<style lang="scss" scoped></style>
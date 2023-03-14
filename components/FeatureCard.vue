<template>
  <div :class="`flex flex-row p-6 rounded-[20px] feature-card ${index !== length - 2 ? ' mb-6' : 'mb-0'}`">
    <div class="w-[64px] h-[64px] rounded-full flexCenter bg-dimBlue">
      <img :src="feature.icon" alt="star" class="w-[50%] h-[50%] object-contain" />
    </div>
    <div class="flex-1 flex flex-col ml-3">
      <h4 class="font-poppins font-semibold text-white text-[18px] leading-[23.4px] mb-1">
        {{ feature.title }}
      </h4>
      <p class="font-poppins font-normal text-dimWhite text-[16px] leading-[24px]">
        {{ feature.content }}
      </p>
    </div>
  </div>
</template>

<script setup>

const { feature, index } = defineProps(['feature', 'index'])

const length = Object.keys(feature).length
</script>

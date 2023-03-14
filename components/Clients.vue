<script setup>
import { clients } from '~~/constants';
</script>

<template>
  <section class="flexCenter my-4">
    <div class="flexCenter flex-wrap w-full">
      <div v-for="client in clients" class="flex-1 flexCenter sm:min-w-[192px] min-w-[120px] m-5" :key="client.id">
        <img class="sm:w-[192px] w-[100px] object-contain" :src="client.logo" :alt="client.id">
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped></style>
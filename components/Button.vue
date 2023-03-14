<template>
  <button type="button"
    :class="`py-4 px-6 bg-blue-gradient font-poppins font-medium text-[18px] text-primary outline-none ${props.styles}`">Get
    Starded
  </button>
</template>

<script setup>
const props = defineProps({
  styles: String,
})
</script>

<style lang="scss" scoped></style>
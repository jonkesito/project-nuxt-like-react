<script setup>
import { close, logo, menu } from '../assets';
import { navLinks } from '../constants';

const toggle = ref(false)

const isToggle = () => {
  if (toggle.value === false) {

    toggle.value = true
    console.log('falso')

  } else {
    toggle.value = false
    console.log('verdadero')
  }

}

</script>



<template>
  <div class="w-full flex py-6 justify-between items-center navbar">
    <img :src="logo" alt="hooback" class="w-[124px] h-[32px]">

    <ul class="list-none sm:flex hidden justify-end items-center flex-1">
      <li v-for="(navLink, index) in navLinks"
        :class="`font-poppins font-normal cursor-pointer text-[16px] ${index === navLinks.length - 1 ? 'mr-0' : 'mr-10'} text-white`"
        :key="navLink.id">
        <a :href="navLink.id">{{ navLink.title }}</a>
      </li>
    </ul>

    <div class="sm:hidden flex flex-1 justify-end items-center text-white">
      <img :src="toggle ? close : menu" alt="menu" class=" w-[28px] h-[28px] object-contain cursor-pointer"
        @click="isToggle()" />
      <div
        :class="`${toggle ? 'flex' : 'hidden'} p-6 bg-black-gradient absolute top-20 right-0 mx-4 my-2 min-w-[140px] rounded-xl sidebar`">
        <ul class="list-none flex flex-col justify-center items-center flex-1">
          <li v-for="(navLink, index) in navLinks"
            :class="`font-poppins font-normal cursor-pointer text-[16px] ${index === navLinks.length - 1 ? 'mb-0' : 'mb-10'} text-white`"
            :key="navLink.id">
            <a :href="navLink.id">{{ navLink.title }}</a>
          </li>
        </ul>
      </div>
    </div>

  </div>
</template>


<style lang="scss" scoped></style>
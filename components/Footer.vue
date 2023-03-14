<template>
  <footer class="flexCenter paddingY flex-col">
    <div class="flexStart md:flex-row flex-col mb-8 w-full">
      <div class="flex-[1] flex flex-col justify-start mr-10">
        <img :src="logo" alt="hooback" class="w-[266px] h-[72.14px] object-contain">
        <p class="paragragh mt-4 max-w-[312px]">
          A new way to make the payments easy, reliable and secure.
        </p>
      </div>

      <div class="flex-[1.5] w-full flex flex-row justify-between flex-wrap md:mt-0 mt-10">
        <div v-for="footerlink in footerLinks" :key="footerlink.id">
          <div class="flex flex-col ss:my-0 my-4 min-w-[150px]">
            <h4 class="font-poppins font-medium text-[18px] leading-[27px] text-white">
              {{ footerlink.title }}
            </h4>
            <ul class="list-none mt-4">
              <li
                :class="`font-poppins font-normal text-[16px] leading-[24px] text-dimWhite hover:text-secondary cursos-pointer 
                                                                                                                                                                                                                                                                                                                  `"
                v-for="link, index in footerlink.links" :key="index">
                {{ link.name }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <div class="w-full flex justify-between items-center md:flex-row flex-col pt-6 border-t-[1px] border-t-[#3F3E45]">
      <p class="font-poppins font-normal text-center text-[18px] leading-[27px] text-white">
        Copyright Ⓒ 2022 HooBank. All Rights Reserved.
      </p>
      <div className="flex flex-row md:mt-0 mt-6">
        <img v-for="(social, index) in socialMedia" :key="index" :src="social.icon" :alt="social.id"
          :class="`w-[21px] h-[21px] object-contain cursor-pointer ${index !== socialMedia.length - 1 ? 'mr-6 ' : 'mr-0'}`"
          @click="() => { window.open(social.link) }" />
      </div>

    </div>
  </footer>
</template>

<script setup>
import { logo } from '~~/assets';
import { footerLinks, socialMedia } from '~~/constants';


</script>

<style lang="scss" scoped></style>
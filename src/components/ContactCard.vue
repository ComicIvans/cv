<script setup lang="ts">
import { computed } from 'vue'
import { useWindowSize } from '@vueuse/core'
import { IconPhone, IconAddressBook, IconMail, IconBrandLinkedin } from '@tabler/icons-vue'

const { width, height } = useWindowSize()
const isMobile = computed(() => width.value < height.value)
</script>

<template>
  <div class="card min-w-fit h-fit bg-base-300 mx-auto mt-3" :class="{ 'text-lg': !isMobile }">
    <div class="card-body items-center text-center">
      <h2 class="card-title text-2xl mb-2">
        <IconAddressBook class="w-8 h-8 text-red-700 stroke-2" />Contacto
      </h2>
      <div class="flex flex-col gap-4">
        <a class="flex flex-row items-center link link-hover" href="tel:+34744481721"
          ><IconPhone class="w-8 h-8 text-red-700 stroke-2 mr-2" />+ 34 744 48 17 21</a
        >
        <a class="flex flex-row items-center link link-hover" href="mailto:isalidocobo@gmail.com"
          ><IconMail class="w-8 h-8 text-red-700 stroke-2 mr-2" />isalidocobo@gmail.com</a
        >
        <a
          class="flex flex-row items-center link link-hover"
          href="https://www.linkedin.com/in/ivansalidocobo/"
          ><IconBrandLinkedin class="w-8 h-8 text-red-700 stroke-2 mr-2" />Iván Salido Cobo</a
        >
      </div>
    </div>
  </div>
</template>

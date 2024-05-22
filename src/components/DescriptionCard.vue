<script setup lang="ts">
import { computed } from 'vue'
import { IconNotes } from '@tabler/icons-vue'
import { useWindowSize } from '@vueuse/core'

const { width, height } = useWindowSize()
const isMobile = computed(() => width.value < height.value)
</script>

<template>
  <div class="card min-w-fit h-fit bg-base-300 mx-auto mt-3" :class="{ 'text-lg': !isMobile }">
    <div class="card-body items-center text-center">
      <h2 class="card-title text-2xl mb-2">
        <IconNotes class="w-8 h-8 text-red-700 stroke-2" />Descripción
      </h2>
      <p>
        Soy un matemático con un fuerte interés en la informática y sus aplicaciones. Me caracterizo
        por ser entusiasta, meticuloso y proactivo. Me adapto rápidamente a nuevas áreas, buscando
        constantemente innovar y encontrar soluciones creativas y efectivas en mis proyectos.
      </p>
    </div>
  </div>
</template>

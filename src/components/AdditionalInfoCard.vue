<script setup lang="ts">
import { IconInfoCircle, IconChevronRight } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
  showLarge: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="showLarge ? 'w-[30rem]' : 'w-96'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconInfoCircle class="w-6 h-6 stroke-2 text-red-700" />Otra información
      </h2>
      <div class="flex flex-col">
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            Tengo un <b>amplio conocimiento normativo</b> sobre el funcionamiento de las
            administraciones públicas y la <b>transparencia.</b>
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            He redactado y ayudado en la
            <b>redacción de varias normativas y reglamentos.</b> Además, estoy participando en la
            <b>reforma de los estatutos de la Universidad.</b>
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            He participado en múltiples <b>negociaciones</b> tanto de normativa como de servicios y
            becas.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

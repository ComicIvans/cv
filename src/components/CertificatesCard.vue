<script setup lang="ts">
import { IconCertificate, IconChevronRight } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
  showLarge: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="showLarge ? 'w-[30rem]' : 'w-[22rem]'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconCertificate class="w-6 h-6 stroke-2 text-red-700" />Certificaciones
      </h2>
      <div class="flex flex-col">
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>Permiso de Conducir:</b> Clase B</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>Inglés:</b> Nivel B2, preparando el C1.</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Data Analyst</b> por Google Cloud Skills Boost. Perfil en
            <a
              href="https://www.cloudskillsboost.google/public_profiles/9db40b9a-29c2-495c-9cb4-f648577ceac6"
              class="link link-hover"
              >este enlace</a
            >.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

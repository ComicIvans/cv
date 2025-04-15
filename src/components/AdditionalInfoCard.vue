<script setup lang="ts">
import { IconPresentation, IconChevronRight } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
  showLarge: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="showLarge ? 'w-[30rem]' : 'w-[22rem]'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconPresentation class="w-6 h-6 stroke-2 text-red-700" />Asistencia a congresos
      </h2>
      <div class="flex flex-col">
        <p class="mb-2">
          He asistido, y cuento con su certificado de aprovechamiento, a múltiples ediciones del
          <a href="https://www.anem.es/web/que-es-el-enem/" class="link link-hover"
            >Encuentro Nacional de Estudiantes de Matemáticas (ENEM)</a
          >, un congreso organizado por y para estudiantes, en las que he podido obtener
          <b>formación adicional en matemáticas, estadística y ciencia de datos</b>. Estas ediciones
          son:
        </p>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>Universidad de Valladolid (2020)</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>Universidad de Murcia (2021)</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>Universidad de Valencia (2022)</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>Universidad de Extremadura (2023)</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            Universidades Carlos III, Complutense, Politécnica y Rey Juan Carlos de Madrid (2024)
          </p>
        </div>
        <p class="my-2">Además, soy <b>organizador</b> del que se celebrará este año en Granada.</p>
        <p>
          Dichos congresos se desarrollan a lo largo de una semana y constan de
          <b>conferencias, talleres y pechakuchas</b>. Además, se establece un contacto con
          distintas empresas a través de un <b>Foro de Empresas</b>.
        </p>
        <p>
          Por otro lado, he asistido al
          <b>VI Congreso CREUP-CRUE y XIV Encuentro de Representantes</b> organizado por CREUP en
          Madrid en 2025. Este evento reúne a Rectores y Vicerrectores con el estudiantado de
          múltiples universidades de España para exponer problemas actuales y buscar soluciones en
          conjunto.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { IconCode } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
  showLarge: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="showLarge ? 'w-[30rem]' : 'w-[23rem]'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconCode class="w-6 h-6 stroke-2 text-red-700" />Proyectos relevantes
      </h2>
      <h3 class="text-lg font-bold text-red-700">Servidor personal</h3>
      <div class="flex flex-col">
        <p>
          Desde 2020 he estado manteniendo un ordeandor en mi casa como servidor personal con Linux.
          Cuenta con varios servicios disponibles a través del dominio
          <a class="link link-hover" href="https://www.wupp.dev/">wup.dev</a> y Docker. Todos los
          servicios que tiene están documentados en
          <a class="link link-hover" href="https://wupp-dev.github.io/server/equipo/historia.html"
            >esta guía</a
          >. Esto me ha permitido obtener conocimientos muy amplios sobre la
          <b>gestión de equipos y de servicios en línea</b>.
        </p>
      </div>
      <h3 class="text-lg font-bold text-red-700">Página web para el III CEEBI</h3>
      <p>
        Además de ayudar en el propio desarrollo del
        <b>III Congreso Estatal de Estudiantes de Biociencias (CEEBI)</b>, desarrollé una web para
        la consulta de los talleres y microcharlas asignados a cada asistente, ver y realizar
        preguntas a los ponentes durante las conferencias y, posteriormente, descargar los
        certificados de asistencia al evento, a los microcursos y de haber presentado pósteres. La
        web se puede consultar en
        <a class="link link-hover" href="https://ceebi.wupp.dev">este enlace</a>.
      </p>
    </div>
  </div>
</template>

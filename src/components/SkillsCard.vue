<script setup lang="ts">
import { IconDeviceDesktop, IconChevronRight } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
  showLarge: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="showLarge ? 'w-[30rem]' : 'w-[22rem]'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconDeviceDesktop class="w-6 h-6 stroke-2 text-red-700" />Conocimientos académicos
      </h2>
      <h3 class="text-lg font-bold text-red-700">Ciberseguridad</h3>
      <div class="flex flex-col">
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Gestión de la ciberseguridad:</b> Coordinación de políticas, procesos y herramientas
            para proteger activos digitales.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Complimiento legislativo:</b> Aplicación de normativas y estándares en materia de
            protección de datos y seguridad.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Diseño y securización de infraestructuras:</b> Planificación y refuerzo de sistemas y
            redes frente a amenazas.
          </p>
        </div>
      </div>
      <h3 class="text-lg font-bold text-red-700">Lenguajes manejados</h3>
      <div class="flex flex-col">
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>JavaScript, HTML y CSS:</b> Aunque he utilizado JavaScript independientemente, suelo
            usar los tres en conjunto para la mayoría de mis proyectos.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Python:</b> He hecho varios scripts y tanto mi TFG ha consistido en hacer un paquete.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>PHP:</b> Mantengo y actualizo varias páginas web con WordPress y Laravel.</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>C++, Java y Rust:</b> Los he utilizado puntualmente para distintos projectos.</p>
        </div>
      </div>
      <h3 class="text-lg font-bold text-red-700">Frameworks y Herramientas</h3>
      <div class="flex flex-col">
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Vue.js:</b> Lo utilizo para la mayoría de mis projectos como, por ejemplo, esta
            página.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Dominios y Google Workspace:</b> Tengo adquirido un dominio y lo llevo gestionando
            varios años. Además, gestiono otros dominios y su Google Workspace como el de la
            asociación <a href="https://www.creup.es" class="link link-hover">CREUP</a>.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

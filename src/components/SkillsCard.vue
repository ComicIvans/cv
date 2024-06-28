<script setup lang="ts">
import { IconDeviceDesktop, IconChevronRight } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="isMobile ? 'w-96' : 'w-[30rem]'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconDeviceDesktop class="w-6 h-6 stroke-2 text-red-700" />Conocimientos informáticos
      </h2>
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
            <b>Python:</b> He hecho varios scripts y mi TFG ha consistido en hacer un paquete con un
            programa de línea de comandos.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>Java:</b> Lo he utilizado para la modificación de plugins de Minecraft.</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>C++, PHP y Rust:</b> Los he utilizado puntualmente para distintos projectos.</p>
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
          <p><b>DNS:</b> Tengo adquirido un dominio y lo llevo gestionando varios años.</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p><b>SQL:</b> He trabajado varias veces con bases de datos SQL.</p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>WordPress:</b> He trabajado con WordPress en la página de la asociación
            <a class="link link-hover" href="https://amatugr.es/">AMAT</a> y actualmente trabajo con
            él en la página de la asociación
            <a class="link link-hover" href="https://creup.es/">CREUP</a>.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Google Workspace y Analytics:</b> He trabajado con Google Workspace en la asociación
            <a class="link link-hover" href="https://amatugr.es/">AMAT</a> y en la
            <a class="link link-hover" href="https://creup.es/">CREUP</a> y con las anlíticas de la
            DEFC y la DGE.
          </p>
        </div>
        <div class="flex flex-row mr-2">
          <IconChevronRight class="min-w-6 w-6 h-6 stroke-2 text-red-700" />
          <p>
            <b>Drupal:</b> Desde 2020 he mantenido las páginas web de la
            <a class="link link-hover" href="https://defc.ugr.es/"
              >Delegación de Estudiantes de la Facultad de Ciencias</a
            >
            y de la
            <a class="link link-hover" href="https://dge.ugr.es/"
              >Delegación General de Estudiantes</a
            >.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

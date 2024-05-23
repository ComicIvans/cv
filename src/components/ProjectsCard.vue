<script setup lang="ts">
import { IconCode } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
}>()
</script>

<template>
  <div class="card bg-base-100 shadow-xl" :class="isMobile ? 'w-96' : 'w-[30rem]'">
    <div class="card-body">
      <h2 class="card-title flex flex-row items-center">
        <IconCode class="w-6 h-6 stroke-2 text-red-700" />Proyectos relevantes
      </h2>
      <h3 class="text-lg font-bold text-red-700">Servidor personal con Linux</h3>
      <div class="flex flex-col">
        <p>
          Desde 2020 he estado manteniendo un ordeandor en mi casa como servidor personal con Linux.
          Cuenta con varios servicios disponibles a través del dominio
          <a class="link link-hover" href="https://www.wupp.dev/">wup.dev</a> y Docker. Todos los
          servicios que tiene están documentados en
          <a class="link link-hover" href="https://wupp-dev.github.io/server/equipo/historia.html"
            >esta guía</a
          >.
        </p>
      </div>
      <h3 class="text-lg font-bold text-red-700">Mantenimiento de páginas web</h3>
      <p>
        Desde 2020 he mantenido las páginas web de la
        <a class="link link-hover" href="https://defc.ugr.es/"
          >Delegación de Estudiantes de la Facultad de Ciencias</a
        >
        y de la
        <a class="link link-hover" href="https://dge.ugr.es/">Delegación General de Estudiantes</a>.
        Especialmente he mantenido los apartados de transparencia. También he editado en varias
        ocasiones la web de la
        <a class="link link-hover" href="https://amatugr.es/">asociación AMAT</a>, hecha con
        WordPress.
      </p>
      <h3 class="text-lg font-bold text-red-700">Firmas de correos</h3>
      <p>
        He elaborado firmas para los correos de la DEFC, la DGE y la asociación AMAT usando Python,
        HTML y CSS. Están disponibles en
        <a class="link link-hover" href="https://github.com/ComicIvans/mail-signatures"
          >este repositorio</a
        >
        de GitHub.
      </p>
      <h3 class="text-lg font-bold text-red-700">Bingo con Andrés</h3>
      <p>
        Para la actividad estrella del patrón de mi Facultad, el Bingo con Andrés Quintana Martín,
        he creado un generador de cartones de bingo con JavaScript, HTML y CSS que se puede ver en
        <a class="link link-hover" href="https://github.com/defcUGR/bingo">este repositorio</a>
        de GitHub. Además, también he hecho con la ayuda de Lucas de Uña Ocampo una página con
        Vue.js para generar y mostrar los resultados del bingo. También se puede consultar en
        <a class="link link-hover" href="https://github.com/defcUGR/bingo-web">este repositorio</a>
        de GitHub.
      </p>
    </div>
  </div>
</template>

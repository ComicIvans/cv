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
      <h3 class="text-lg font-bold text-red-700">Paquete de Python</h3>
      <p>
        Mi TFG ha consistido en la creación de un paquete de Pyhton llamado
        <code>polyharmonics</code> que permite el cálculo simbólico, la evaluación, la
        representación y la comparación de rendimiento entre métodos de cálculo y evaluación de
        varios tipos de funciones. Está disponible en
        <a class="link link-hover" href="https://github.com/ComicIvans/polyharmonics"
          >este repositorio</a
        >
        de GitHub.
      </p>
      <h3 class="text-lg font-bold text-red-700">Bingo con Andrés</h3>
      <p>
        Para la actividad estrella del patrón de mi Facultad, el Bingo con Andrés Quintana Martín,
        he creado un generador de cartones de bingo con JavaScript, HTML y CSS que se puede ver en
        <a class="link link-hover" href="https://github.com/defcUGR/bingo">este repositorio</a>
        de GitHub. Además, también he hecho con la ayuda de
        <a href="https://www.linkedin.com/in/deunaocampo/" class="link link-hover"
          >Lucas de Uña Ocampo</a
        >
        una página con Vue.js para generar y mostrar los resultados del bingo. También se puede
        consultar en
        <a class="link link-hover" href="https://github.com/defcUGR/bingo-web">este repositorio</a>
        de GitHub.
      </p>
      <h3 class="text-lg font-bold text-red-700">Registro de asistencia</h3>
      <p>
        Una aplicación de escritorio desarrollada junto con
        <a href="https://www.linkedin.com/in/deunaocampo/" class="link link-hover"
          >Lucas de Uña Ocampo</a
        >
        para gestionar el censo de la Delegación de Estudiantes de la Facultad de Ciencias (DEFC) y
        registrar la asistencia a sus reuniones. Está disponible en
        <a class="link link-hover" href="https://github.com/defcUGR/asistencia">este repositorio</a>
        de GitHub.
      </p>
      <h3 class="text-lg font-bold text-red-700">Gestión de entradas de graduaciones</h3>
      <p>
        Una aplicación de escritorio en desarrollo junto con
        <a href="https://www.linkedin.com/in/deunaocampo/" class="link link-hover"
          >Lucas de Uña Ocampo</a
        >
        para generar y validar entradas para las graduaciones. Está disponible en
        <a class="link link-hover" href="https://github.com/defcUGR/graduaciones"
          >este repositorio</a
        >
        de GitHub.
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
    </div>
  </div>
</template>

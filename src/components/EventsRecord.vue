<script setup lang="ts">
import { IconCalendarEvent } from '@tabler/icons-vue'

defineProps<{
  isMobile: boolean
}>()
</script>

<template>
  <div class="flex flex-col items-center justify-center">
    <div class="flex flex-row text-xl font-bold bg-base-300 rounded-xl w-fit p-4 mb-2 items-center">
      <IconCalendarEvent class="w-6 h-6 text-red-700 stroke-2 mr-2" />
      <h2>Eventos organizados</h2>
    </div>
    <ul
      :class="{ 'timeline-compact': isMobile }"
      class="timeline timeline-snap-icon timeline-vertical mx-auto"
    >
      <li>
        <div class="timeline-middle text-primary">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="h-5 w-5"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
              clip-rule="evenodd"
            />
          </svg>
        </div>
        <div :class="{ 'text-end': !isMobile }" class="timeline-start mb-10">
          <time class="italic">Marzo de 2023</time>
          <div class="text-lg font-black">AGO de la ANEM</div>
          Organicé, junto a otras tres personas, una asamblea general ordinaria de la Asociación
          Nacional de Estudiantes de Matemáticas (ANEM), evento al que asistieron alrededor de 60
          personas. Mis labores consistieron principalmente en gestionar los pagos de los diferentes
          organizadores, organizar los coffee breaks y solicitar reservas de espacios.
        </div>
        <hr class="bg-primary" />
      </li>
      <li>
        <hr class="bg-primary" />
        <div class="timeline-middle text-primary">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="h-5 w-5"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
              clip-rule="evenodd"
            />
          </svg>
        </div>
        <div class="timeline-end mb-10">
          <time class="italic">Noviembre de 2023</time>
          <div class="text-lg font-black">San Alberto 2023</div>
          Aunque es un evento en el que llevo participando desde 2019, en esta edición del patrón de
          mi Facultad me impliqué más que nunca en su organización. Me encargué, junto a otra
          persona, de organizar la actividad estrella, el bingo con Andrés Quintana Martín, al que
          acudieron alrededor de 300 personas. La organización de la actividad consistió en la
          creación de los cartones de bingo mediante HTML, CSS Y JavaScript
          <a class="link link-hover" href="https://github.com/defcUGR/bingo">(consultar código)</a>
          y la creación de una plataforma web para poder mostrar los resultados
          <a class="link link-hover" href="https://github.com/defcUGR/bingo-web"
            >(consultar código)</a
          >.
        </div>
        <hr class="bg-primary" />
      </li>
      <li>
        <hr class="bg-primary" />
        <div class="timeline-middle text-primary">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="h-5 w-5"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
              clip-rule="evenodd"
            />
          </svg>
        </div>
        <div :class="{ 'text-end': !isMobile }" class="timeline-start mb-10">
          <time class="italic">Abril de 2024</time>
          <div class="text-lg font-black">XIII AGO de ACUA</div>
          Como Director de Relaciones Externas, ayudé en la organización de la XIII asamblea general
          ordinaria de la asamblea de consejos universitarios de Andalucía, a la que asistieron
          alrededor de 20 personas. Me encargué principalmente de la organización de los coffee
          breaks, la gestión de las comidas y la posterior tramitación de facturas.
        </div>
        <hr class="bg-primary" />
      </li>
      <li>
        <hr />
        <div class="timeline-middle text-primary">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="h-5 w-5"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
              clip-rule="evenodd"
            />
          </svg>
        </div>
        <div class="timeline-end mb-10">
          <time class="italic">Noviembre de 2024</time>
          <div class="text-lg font-black">LXXVI AGO de CREUP</div>
          He sido el principal organizador de la 77.ª Asamblea General Ordinaria de CREUP,
          coordinando las reservas de espacios y contactos con los diferentes órganos implicados.
          Además, me encargué de la gestión económica del evento y la búsqueda de financiación.
        </div>
        <hr class="bg-primary" />
      </li>
      <li>
        <hr />
        <div class="timeline-middle">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="h-5 w-5"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
              clip-rule="evenodd"
            />
          </svg>
        </div>
        <div :class="{ 'text-end': !isMobile }" class="timeline-start mb-10">
          <time class="italic">Julio de 2025</time>
          <div class="text-lg font-black">XXVI ENEM</div>
          Soy Tesorero y Secretario del Comité Organizador del XXVI Encuentro Nacional de
          Estudiantes de Matemáticas (ENEM), que reúne todos los años a cientos de estudiantes de
          Matemáticas, Estadística y Ciencia de Datos de toda España. Estos encuentros cuentan con
          un enfoque tanto académico como profesional, permitiendo el contacto directo con empresas
          del sector.
        </div>
      </li>
    </ul>
  </div>
</template>

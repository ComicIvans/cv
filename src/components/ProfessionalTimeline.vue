<script setup lang="ts">
import { computed } from 'vue'
import { IconBuildingBank } from '@tabler/icons-vue'
import { useWindowSize } from '@vueuse/core'

const { width, height } = useWindowSize()
const isMobile = computed(() => width.value < height.value)
</script>

<template>
  <div class="flex flex-col items-center justify-center">
    <div class="flex flex-row text-xl font-bold bg-base-300 rounded-xl w-fit p-4 mb-2 items-center">
      <IconBuildingBank class="w-6 h-6 text-red-700 stroke-2 mr-2" />
      <h2>Trayectoria en representación</h2>
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
          <time class="italic">Diciembre de 2020</time>
          <div class="text-lg font-black">Inicio como miembro</div>
          Comencé mis peripecias como miembro de pleno derecho en el Claustro Universitairo, en mi
          MORE, la Delegación General de Estudiantes (DGE), y, por consiguiente, en la Delegación de
          Estudiantes de la Facultad de Ciencias (DEFC). En esta fecha también pasé a ser
          <b>Tesorero de la DGE</b> y <b>Secretario de la DEFC</b>.
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
          <time class="italic">Diciembre de 2022</time>
          <div class="text-lg font-black">Final de mi primer mandato</div>
          Finalizó el mandato tanto de la DGE como de la DEFC, por lo que dejé los cargos de
          Secretario y Tesorero tras dos años de de intenso trabajo y dedicación. Aun así, seguí
          como miembro en el siguiente mandato, el actual, ya que el mandato del Claustro
          Universitario es de cuatro años. Esto me permitió entrar en ese mismo mes al
          <b>Consejo de Gobierno</b>, donde todavía sigo.
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
          <time class="italic">Marzo de 2023</time>
          <div class="text-lg font-black">Director de Relaciones Externas</div>
          Para mejorar la gestión de las relaciones externas de la DGE, se creó el cargo de Director
          de Relaciones Externas, el cual asumí por mi experiencia en la gestión de los viajes y el
          contacto con otras entidades. En este cargo, he podido incrementar la participación de la
          DGE en eventos y reuniones externas así como afianzar su presencia en el panorama
          nacional.
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
          <time class="italic">Junio de 2023</time>
          <div class="text-lg font-black">Vicecoordinador Académico</div>
          Cuando hubo que presentar un nuevo equipo para la Comisión Permanente de la DGE, decidí
          formar parte de este como Vicecoordinador Académico, cargo que me ha permitido contribuir
          de manera directa a la mejora de la calidad de la docencia y la adquisición de nuevas
          garantías y derechos para la evaluación del estudiantado.
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
          <time class="italic">Junio de 2024</time>
          <div class="text-lg font-black">Vocal de Digitalización y Transparencia</div>
          La Vocalía que pretendo ocupar es la de Digitalización y Transparencia, en la que
          trabajaré por mantener la transparencia de la web de la CREUP y por mejorar su
          funcionamiento. Además, me gustaría trabajar en mejorar la intranet para añadir
          funcionalidades y mejorar su aspecto.
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, computed } from 'vue'
import {
  IconPhone,
  IconChevronDown,
  IconChevronUp,
  IconUser,
  IconSchool,
  IconBuildingBank,
  IconCertificate
} from '@tabler/icons-vue'
import { useWindowSize } from '@vueuse/core'

const move_x = ref(true)
const menuOpened = ref(false)
const tabs = [
  { name: 'Sobre mí', icon: IconUser },
  { name: 'Estudios y conocimientos', icon: IconSchool },
  { name: 'Representación y eventos', icon: IconBuildingBank },
  { name: 'Certificaciones y otros', icon: IconCertificate }
]
const activeTab = ref('Sobre mí')
const { width, height } = useWindowSize()
const isMobile = computed(() => width.value < height.value)

onMounted(() => {
  setTimeout(() => {
    move_x.value = false
  }, 500)
})
</script>

<template>
  <div class="w-11/12 mx-auto p-6" v-auto-animate>
    <div v-if="move_x" class="mt-36 opacity-0 transition-opacity duration-500"></div>
    <header
      class="text-center mb-8 opacity-0 transition-opacity duration-500"
      :class="{
        'opacity-100': !move_x,
        'text-center': isMobile,
        'flex flex-row items-center': !isMobile
      }"
    >
      <img
        class="rounded-full w-32 h-32 border-4 border-red-700"
        :class="{ 'mx-auto': isMobile }"
        src="@/assets/profile-pic.jpg"
        alt="Iván Salido Cobo"
      />
      <div class="mx-auto" v-if="!isMobile">
        <ul
          :class="width > 1400 ? 'menu-horizontal' : 'menu-vertical'"
          class="menu bg-base-200 rounded-box"
        >
          <li v-for="(tab, index) in tabs" :key="index">
            <a
              v-auto-animate
              :class="activeTab == tab.name ? 'active' : ''"
              @click="
                () => {
                  activeTab = tab.name
                  menuOpened = false
                }
              "
              ><component :is="tab.icon" class="w-4 h-4 stroke-2 mr-1" />{{ tab.name }}</a
            >
          </li>
        </ul>
      </div>
      <div class="flex flex-col itmes-center" :class="{ 'text-right': !isMobile }">
        <h1 class="text-4xl font-bold mt-4 text-red-700">Iván Salido Cobo</h1>
        <p class="text-xl text-gray-600">Matemático</p>
      </div>
      <div class="mx-auto" v-if="isMobile" v-auto-animate>
        <ul v-if="menuOpened" class="menu menu-vertical bg-base-200 rounded-box w-fit mx-auto mt-4">
          <li>
            <a @click="menuOpened = false" class="justify-between"
              >Contenido<IconChevronUp class="w-4 h-4 stroke-2"
            /></a>
          </li>
          <li v-for="(tab, index) in tabs" :key="index">
            <a
              v-auto-animate
              :class="activeTab == tab.name ? 'active' : ''"
              @click="
                () => {
                  activeTab = tab.name
                  menuOpened = false
                }
              "
              ><component :is="tab.icon" class="w-4 h-4 stroke-2 mr-1" />{{ tab.name }}</a
            >
          </li>
        </ul>
        <ul v-else class="menu menu-vertical bg-base-200 rounded-box w-fit mx-auto mt-4">
          <li>
            <a @click="menuOpened = true">Contenido<IconChevronDown class="w-4 h-4 stroke-2" /></a>
          </li>
        </ul>
      </div>
    </header>
    <div class="divider"></div>
    <div
      class="grid gap-8 opacity-0 transition-opacity duration-500"
      :class="{ 'opacity-100': !move_x, 'grid-cols-1': isMobile, 'grid-cols-2': !isMobile }"
    >
      <div>
        <section v-if="activeTab == 'Sobre mí'" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Contacto
          </h2>
          <p>
            <IconPhone class="w-8 h-8" /><a
              href="tel:+34744481721"
              class="text-red-700 hover:underline"
              >+34 744 48 17 21</a
            >
          </p>
          <p>
            <i class="ti ti-mail mr-2"></i
            ><a href="mailto:isalidocobo@gmail.com" class="text-red-700 hover:underline"
              >isalidocobo@gmail.com</a
            >
          </p>
          <p>
            <i class="ti ti-brand-linkedin mr-2"></i
            ><a href="https://www.linkedin.com/in/comicivans/" class="text-red-700 hover:underline"
              >LinkedIn</a
            >
          </p>
          <p>
            <i class="ti ti-brand-github mr-2"></i
            ><a href="https://github.com/ComicIvans/" class="text-red-700 hover:underline"
              >GitHub</a
            >
          </p>
        </section>

        <section v-if="activeTab == 'Sobre mí'" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Sobre mí
          </h2>
          <p>
            Matemático apasionado por la informática, proactivo y meticuloso. Aprendo rápidamente y
            busco constantemente innovar y mejorar.
          </p>
        </section>

        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Estudios
          </h2>
          <p>Grado en Matemáticas | Universidad de Granada | Septiembre 2019 - Presente</p>
          <p>Créditos restantes: 12 ECTS + TFG (12 ECTS)</p>
        </section>

        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Certificaciones
          </h2>
          <p>Data Analyst por Google Cloud | Skills Boost</p>
        </section>

        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Conocimientos informáticos
          </h2>
          <p>
            <strong>Lenguajes manejados:</strong> JavaScript, HTML, CSS, Python, Java, C++, PHP,
            Rust
          </p>
          <p>
            <strong>Frameworks y Herramientas:</strong> Vue.js, DNS, SQL, WordPress, Google
            Workspace y Analytics
          </p>
        </section>
      </div>

      <div v-if="false">
        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Experiencia y cargos
          </h2>
          <ul class="list-disc list-inside">
            <li>Vice. Académico del MORE | Junio 2023 - Presente</li>
            <li>Director de Externas del MORE | Marzo 2023 - Presente</li>
            <li>Consejero de Gobierno | Diciembre 2022 - Presente</li>
            <li>
              Tesorero del MORE y Secretario de la Delegación de Estudiantes | Diciembre 2020 -
              Diciembre 2022
            </li>
            <li>Miembro del Claustro y MORE | Diciembre 2020 - Presente</li>
          </ul>
        </section>

        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Organización de eventos
          </h2>
          <ul class="list-disc list-inside">
            <li>XXVI ENEM, Julio 2025</li>
            <li>LXXVI AGO CREUP, Noviembre 2024</li>
            <li>XIII AGO ACUA, Abril 2024</li>
            <li>AGO ANEM, Marzo 2023</li>
          </ul>
        </section>

        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Proyectos relevantes
          </h2>
          <p>
            Servidor personal con Linux y Docker:
            <a href="https://wupp.dev/" target="_blank" class="text-red-700 hover:underline"
              >wupp.dev</a
            >
          </p>
          <p>
            Mantenimiento y actualización de páginas web del MORE y Delegación de Estudiantes de la
            Facultad de Ciencias
          </p>
          <p>
            Firmas de correos con HTML y CSS:
            <a
              href="https://github.com/ComicIvans/mail-signatures"
              target="_blank"
              class="text-red-700 hover:underline"
              >GitHub</a
            >
          </p>
        </section>

        <section v-if="false" class="mb-8">
          <h2 class="text-2xl font-bold border-b-2 border-gray-300 pb-2 mb-4 text-red-700">
            Más información
          </h2>
          <p>Permiso de Conducir: Clase B</p>
          <p>Inglés: Nivel B2</p>
        </section>
      </div>
    </div>
  </div>
</template>

<style scoped>
.opacity-0 {
  opacity: 0;
}
.opacity-100 {
  opacity: 1;
}
.transition-opacity {
  transition: opacity 1s ease-in-out;
}
</style>

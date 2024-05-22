<script setup lang="ts">
import { ref, onMounted, computed } from 'vue'
import {
  IconChevronDown,
  IconChevronUp,
  IconUser,
  IconSchool,
  IconBuildingBank,
  IconCertificate,
  IconCopyright,
  IconBrandInstagram,
  IconBrandX,
  IconBrandGithub
} from '@tabler/icons-vue'
import { useWindowSize } from '@vueuse/core'
import jokes from '@/assets/jokes.json'
import ContactCard from '@/components/ContactCard.vue'
import DescriptionCard from '@/components/DescriptionCard.vue'
import ProfessionalTimeline from '@/components/ProfessionalTimeline.vue'
import EventsRecord from '@/components/EventsRecord.vue'

const movex = ref(true)
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
const currJoke = ref('')
const newJoke = () => {
  currJoke.value = jokes[Math.floor(Math.random() * jokes.length)]
}

onMounted(() => {
  setTimeout(() => {
    movex.value = false
  }, 500)
})
</script>

<template>
  <div class="min-w-screen min-h-screen flex flex-col bg-base-200">
    <main class="flex-grow">
      <dialog id="joke" class="modal">
        <div class="modal-box">
          <h3 class="font-bold text-lg">También soy un chistoso</h3>
          <p class="py-4">{{ currJoke || '¡Vaya! No se ha podido cargar ningún chiste :(' }}</p>
        </div>
        <form method="dialog" class="modal-backdrop">
          <button>close</button>
        </form>
      </dialog>
      <div class="w-11/12 mx-auto p-6" v-auto-animate>
        <div v-if="movex" class="mt-36 opacity-0 transition-opacity duration-500"></div>
        <header
          class="text-center mb-8 opacity-0 transition-opacity duration-500"
          :class="{
            'opacity-100': !movex,
            'text-center': isMobile,
            'flex flex-row items-center': !isMobile
          }"
        >
          <button @click="newJoke" onclick="joke.showModal()">
            <img
              class="rounded-full w-32 h-32 border-4 border-red-700 btn btn-ghost p-0"
              :class="{ 'mx-auto': isMobile }"
              src="@/assets/profile-pic.jpg"
              alt="Iván Salido Cobo"
            />
          </button>
          <div class="mx-auto" v-if="!isMobile">
            <ul
              :class="width > 1400 ? 'menu-horizontal' : 'menu-vertical'"
              class="menu bg-base-200 rounded-box border-2 border-base-300"
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
            <p class="text-xl text-gray-600">Graduado en Matemáticas</p>
          </div>
          <div class="mx-auto" v-if="isMobile" v-auto-animate>
            <ul
              v-if="menuOpened"
              class="menu menu-vertical bg-base-200 rounded-box w-fit mx-auto mt-4 border-2 border-base-300"
            >
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
            <ul
              v-else
              class="menu menu-vertical bg-base-200 rounded-box w-fit mx-auto mt-4 border-2 border-base-300"
            >
              <li>
                <a @click="menuOpened = true"
                  >Contenido<IconChevronDown class="w-4 h-4 stroke-2"
                /></a>
              </li>
            </ul>
          </div>
        </header>
        <div
          class="divider opacity-0 transition-opacity duration-500"
          :class="{ 'opacity-100': !movex }"
        ></div>
        <div
          class="grid gap-8 opacity-0 transition-opacity duration-500"
          :class="{ 'opacity-100': !movex, 'grid-cols-1': isMobile, 'grid-cols-2': !isMobile }"
        >
          <ContactCard v-if="activeTab == 'Sobre mí'" />
          <DescriptionCard v-if="activeTab == 'Sobre mí'" />
          <ProfessionalTimeline v-if="activeTab == 'Representación y eventos'" />
          <EventsRecord v-if="activeTab == 'Representación y eventos'" />
        </div>
      </div>
    </main>
    <footer
      class="footer items-center p-4 bg-base-300 opacity-0 transition-opacity duration-500"
      :class="{ 'opacity-100': !movex }"
    >
      <aside class="items-center grid-flow-col">
        <IconCopyright class="w-6 h-6" />
        <p>
          Desarrollado por Iván Salido Cobo bajo la licencia MIT. Consulta el código en
          <a class="link link-hover" href="https://github.com/ComicIvans/cv">GitHub</a>.
        </p>
      </aside>
      <nav class="grid-flow-col gap-4 md:place-self-center md:justify-self-end">
        <a class="link link-hover" href="https://www.instagram.com/comic.ivans/"
          ><IconBrandInstagram class="w-8 h-8"
        /></a>
        <a class="link link-hover" href="https://x.com/comic_ivans"
          ><IconBrandX class="w-8 h-8"
        /></a>
        <a class="link link-hover" href="https://github.com/ComicIvans/"
          ><IconBrandGithub class="w-8 h-8"
        /></a>
      </nav>
    </footer>
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

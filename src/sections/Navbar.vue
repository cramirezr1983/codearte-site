<script setup>
import { ref } from 'vue'
import logo from '../assets/logo/CodeArteLogo.png'

const mobileMenu = ref(false)

const closeMenu = () => {
  mobileMenu.value = false
}
</script>

<template>
  <header
      class="sticky top-0 z-50 border-b border-gray-200 bg-white/80 backdrop-blur-md"
  >
    <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">

      <!-- Logo -->

      <a
          href="#"
          class="flex items-center gap-3"
      >
        <img
            :src="logo"
            alt="CodeArte"
            class="h-12 w-auto"
        />

        <span class="text-2xl font-bold tracking-tight">
    CodeArte
  </span>
      </a>

      <!-- Desktop Menu -->

      <nav class="hidden md:flex gap-8 text-sm font-medium">

        <a
            href="#services"
            class="hover:text-gray-500 transition"
        >
          Servicios
        </a>

        <a
            href="#experience"
            class="hover:text-gray-500 transition"
        >
          Experiencia
        </a>

        <a
            href="#portfolio"
            class="hover:text-gray-500 transition"
        >
          Proyectos
        </a>

        <a
            href="#contact"
            class="hover:text-gray-500 transition"
        >
          Contacto
        </a>

      </nav>

      <!-- Mobile Button -->

      <button
          @click="mobileMenu = !mobileMenu"
          class="md:hidden text-2xl"
      >
        ☰
      </button>

    </div>

    <!-- Mobile Menu -->

    <div
        v-if="mobileMenu"
        class="md:hidden border-t border-gray-200 bg-white"
    >

      <nav class="flex flex-col px-6 py-6 gap-6 text-sm font-medium">

        <a
            href="#services"
            @click="closeMenu"
            class="hover:text-gray-500 transition"
        >
          Servicios
        </a>

        <a
            href="#experience"
            @click="closeMenu"
            class="hover:text-gray-500 transition"
        >
          Experiencia
        </a>

        <a
            href="#portfolio"
            @click="closeMenu"
            class="hover:text-gray-500 transition"
        >
          Proyectos
        </a>

        <a
            href="#contact"
            @click="closeMenu"
            class="hover:text-gray-500 transition"
        >
          Contacto
        </a>

      </nav>

    </div>

  </header>
</template>
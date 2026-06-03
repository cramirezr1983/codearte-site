<script setup>
import logo from '../assets/logo/CodeArteLogo.png'
</script>
<template>
  <footer class="border-t border-gray-200 py-10 px-6">

    <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">

      <div>
        <div class="flex items-center gap-3 mb-2">

          <img
              :src="logo"
              alt="CodeArte"
              class="h-14 w-auto"
          />

          <h3 class="text-2xl font-bold tracking-tight">
            CodeArte
          </h3>

        </div>

        <p class="text-gray-600 text-sm">
          Desarrollo web, e-commerce e integraciones modernas.
        </p>
      </div>

      <div class="flex items-center gap-6 text-sm text-gray-600">

        <a
            href="#services"
            class="hover:text-black transition"
        >
          Servicios
        </a>

        <a
            href="#experience"
            class="hover:text-black transition"
        >
          Experiencia
        </a>

        <a
            href="#portfolio"
            class="hover:text-black transition"
        >
          Proyectos
        </a>

        <a
            href="#contact"
            class="hover:text-black transition"
        >
          Contacto
        </a>

      </div>

    </div>

  </footer>
</template>
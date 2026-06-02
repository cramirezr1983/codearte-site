<script setup>
import erikalImg from '../assets/projects/erikal.png'
</script>
<template>
  <section
      id="portfolio"
      class="py-24 px-6 border-t border-gray-200"
  >
    <div class="max-w-7xl mx-auto">

      <div class="max-w-3xl mb-16">

        <p class="text-sm uppercase tracking-[0.2em] text-gray-500 mb-4">
          Proyectos
        </p>

        <h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-6">
          Proyectos recientes y sitios en desarrollo
        </h2>

        <p class="text-lg text-gray-600 leading-relaxed">
          Algunos de los proyectos, plataformas y experiencias digitales
          en las que estamos trabajando actualmente.
        </p>

      </div>

      <div class="grid lg:grid-cols-3 gap-8">

        <!-- Proyecto 1 -->

        <div class="border border-gray-200 rounded-3xl overflow-hidden">

          <a href="https://erikal.cl" target="_blank"><img
              :src="erikalImg"
              alt="Erikal"
              class="h-56 w-full object-cover"
          /></a>

          <div class="p-8">

            <h3 class="text-2xl font-semibold mb-4">
              Erikal
            </h3>

            <!--p class="text-gray-600 leading-relaxed mb-6">
              Sitio corporativo y presencia digital moderna enfocada
              en identidad visual y experiencia de usuario.
            </p-->
            <p class="text-gray-600 leading-relaxed mb-6">
              Artesana de la localidad de Coñaripe, donde se exponen algunos de
              los trabajos realizados con toda la suavidad de la lana natural.
            </p>

            <div class="flex flex-wrap gap-3">

              <span class="border border-gray-300 px-3 py-1 rounded-full text-sm">
                Vue
              </span>

              <span class="border border-gray-300 px-3 py-1 rounded-full text-sm">
                Tailwind
              </span>

            </div>

          </div>

        </div>

        <!-- Proyecto 2 -->

        <div class="border border-gray-200 rounded-3xl overflow-hidden">

          <div class="h-56 bg-gray-100"></div>

          <div class="p-8">

            <h3 class="text-2xl font-semibold mb-4">
              Portfolio Fotográfico
            </h3>

            <p class="text-gray-600 leading-relaxed mb-6">
              Plataforma visual optimizada para galerías, fotografía
              y contenido multimedia.
            </p>

            <div class="flex flex-wrap gap-3">

              <span class="border border-gray-300 px-3 py-1 rounded-full text-sm">
                Frontend
              </span>

              <span class="border border-gray-300 px-3 py-1 rounded-full text-sm">
                Responsive
              </span>

            </div>

          </div>

        </div>

        <!-- Proyecto 3 -->

        <div class="border border-gray-200 rounded-3xl overflow-hidden">

          <div class="h-56 bg-gray-100"></div>

          <div class="p-8">

            <h3 class="text-2xl font-semibold mb-4">
              Landing para Banda
            </h3>

            <p class="text-gray-600 leading-relaxed mb-6">
              Sitio promocional para difusión musical, contenido multimedia
              y presencia digital.
            </p>

            <div class="flex flex-wrap gap-3">

              <span class="border border-gray-300 px-3 py-1 rounded-full text-sm">
                UI/UX
              </span>

              <span class="border border-gray-300 px-3 py-1 rounded-full text-sm">
                Web
              </span>

            </div>

          </div>

        </div>

      </div>

    </div>
  </section>
</template>
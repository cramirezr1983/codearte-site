<script setup>
import heroBg from '../assets/hero/bg-deskk.png'
</script>

<template>

  <section class="relative overflow-hidden">

    <!-- Background -->

    <div class="absolute inset-0">

      <img
          :src="heroBg"
          alt=""
          class="w-full h-full object-cover opacity-00"
      />

      <div class="absolute inset-0 bg-black/20"></div>

    </div>

    <!-- Content -->

    <div class="relative z-10 px-6 pt-10 pb-14 md:pt-16 md:pb-24">

      <div class="max-w-5xl mx-auto text-center">

        <p class="text-sm uppercase tracking-[0.2em] text-gray-400 mb-6">
          Desarrollo Web · E-commerce · Integraciones
        </p>

        <h1 class="text-4xl md:text-7xl font-bold tracking-tight leading-tight mb-8 text-white">
          Creamos sitios web rápidos, modernos y escalables
        </h1>

        <p class="text-lg md:text-xl text-gray-300 max-w-3xl mx-auto mb-10 leading-relaxed">
          Desarrollamos sitios web, e-commerce, integraciones y soluciones
          digitales enfocadas en rendimiento, escalabilidad, experiencia de usuario,
          con enfoque técnico y creativo.
        </p>

        <div class="flex flex-col sm:flex-row gap-4 justify-center">

          <a
              href="#contact"
              class="bg-white text-black px-8 py-4 rounded-xl font-medium hover:opacity-90 transition hover:scale-[1.02]"
          >
            Hablemos
          </a>

          <a
              href="#portfolio"
              class="border border-gray-500 text-white px-8 py-4 rounded-xl font-medium hover:bg-white/10 transition hover:scale-[1.02]"
          >
            Ver proyectos
          </a>

        </div>

      </div>

    </div>

  </section>

</template>
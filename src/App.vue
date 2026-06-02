<script setup>
import Navbar from './sections/Navbar.vue'
import Hero from './sections/Hero.vue'
import Services from './sections/Services.vue'
import Experience from './sections/Experience.vue'
import Portfolio from './sections/Portfolio.vue'
import Contact from "./sections/Contact.vue";
import Footer from './sections/Footer.vue'

import BackToTop from './components/BackToTop.vue'
import WhatsappButton from './components/WhatsappButton.vue'
</script>

<template>
  <div class="bg-white text-gray-900">

    <Navbar />

    <Hero />

    <Services />

    <Experience />

    <Portfolio />

    <Contact/>

    <Footer/>

    <BackToTop />
    <WhatsappButton/>

  </div>
</template>
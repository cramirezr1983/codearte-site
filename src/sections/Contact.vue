<template>
  <section
      id="contact"
      class="py-24 px-6 border-t border-gray-200"
  >
    <div class="max-w-4xl mx-auto text-center">

      <p class="text-sm uppercase tracking-[0.2em] text-gray-500 mb-4">
        Contacto
      </p>

      <h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-6">
        Hablemos sobre tu próximo proyecto
      </h2>

      <p class="text-lg text-gray-600 leading-relaxed mb-12">
        Sitios web, e-commerce, integraciones o soporte técnico.
        Estamos disponibles para ayudarte a desarrollar soluciones modernas y escalables.
      </p>

      <!-- Formulario -->

      <form
          action="https://api.web3forms.com/submit"
          method="POST"
          class="space-y-6 text-left"
      >

        <input
            type="hidden"
            name="access_key"
            value="064bdc1a-7e48-4bcd-8d70-072703ad7384"
        />

        <div>
          <label class="block mb-2 text-sm font-medium">
            Nombre
          </label>

          <input
              type="text"
              name="name"
              required
              class="w-full border border-gray-300 rounded-xl px-4 py-4 focus:outline-none focus:border-black transition"
          />
        </div>

        <div>
          <label class="block mb-2 text-sm font-medium">
            Correo electrónico
          </label>

          <input
              type="email"
              name="email"
              required
              class="w-full border border-gray-300 rounded-xl px-4 py-4 focus:outline-none focus:border-black transition"
          />
        </div>

        <div>
          <label class="block mb-2 text-sm font-medium">
            Mensaje
          </label>

          <textarea
              name="message"
              rows="6"
              required
              class="w-full border border-gray-300 rounded-xl px-4 py-4 focus:outline-none focus:border-black transition"
          ></textarea>
        </div>

        <button
            type="submit"
            class="bg-black text-white px-8 py-4 rounded-xl font-medium hover:opacity-90 transition"
        >
          Enviar mensaje
        </button>

      </form>

      <!-- Contacto directo -->

      <div class="mt-16 flex flex-col md:flex-row items-center justify-center gap-6 text-gray-600">

        <a
            href="mailto:contacto@webcore.cl"
            class="hover:text-black transition"
        >
          contacto@webcore.cl
        </a>

        <span class="hidden md:block">
          ·
        </span>

        <a
            href="https://linkedin.com"
            target="_blank"
            class="hover:text-black transition"
        >
          LinkedIn
        </a>

        <span class="hidden md:block">
          ·
        </span>

        <a
            href="https://wa.me/56952544392"
            target="_blank"
            class="hover:text-black transition"
        >
          WhatsApp
        </a>

      </div>

    </div>
  </section>
</template>
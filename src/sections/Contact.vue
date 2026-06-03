<script setup>
import { reactive, ref } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const loading = ref(false)
const success = ref(false)
const error = ref('')

const validateEmail = (email) => {
  return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)
}

const handleSubmit = async () => {

  error.value = ''
  success.value = false

  if (!form.name || !form.email || !form.message) {
    error.value = 'No llenaste todos los campos.'
    return
  }

  if (!validateEmail(form.email)) {
    error.value = 'Ingresa un correo válido.'
    return
  }

  loading.value = true

  try {

    const response = await fetch(
        'https://api.web3forms.com/submit',
        {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({
            access_key: '064bdc1a-7e48-4bcd-8d70-072703ad7384',
            name: form.name,
            email: form.email,
            message: form.message
          })
        }
    )

    const data = await response.json()

    if (data.success) {

      success.value = true

      // Limpiar formulario

      form.name = ''
      form.email = ''
      form.message = ''

    } else {

      error.value = 'No se pudo enviar el mensaje.'

    }

  } catch (err) {

    error.value = 'Ocurrió un error inesperado.'

  } finally {

    loading.value = false

  }

}
</script>

<template>

  <section
      id="contact"
      class="py-20 px-6"
  >

    <div class="max-w-3xl mx-auto">

      <div class="text-center mb-12">

        <h2 class="text-4xl font-bold tracking-tight mb-4">
          Hablemos sobre tu próximo proyecto :)
        </h2>
        <h3>Cuéntanos sobre tu proyecto o idea.</h3>
        <p class="text-gray-600">
          Sitios web, e-commerce, integraciones, soporte técnico, mantenimiento.
          -Estamos disponibles para ayudarte a desarrollar soluciones modernas y escalables.
        </p>

      </div>

      <form
          @submit.prevent="handleSubmit"
          class="space-y-6"
      >

        <div>

          <input
              v-model="form.name"
              type="text"
              placeholder="Nombre"
              class="w-full border border-gray-300 rounded-xl px-5 py-4 outline-none focus:border-black transition"
          />

        </div>

        <div>

          <input
              v-model="form.email"
              type="email"
              placeholder="Correo electrónico"
              class="w-full border border-gray-300 rounded-xl px-5 py-4 outline-none focus:border-black transition"
          />

        </div>

        <div>

          <textarea
              v-model="form.message"
              rows="6"
              placeholder="Cuéntanos sobre tu proyecto"
              class="w-full border border-gray-300 rounded-xl px-5 py-4 outline-none focus:border-black transition resize-none"
          ></textarea>

        </div>

        <button
            type="submit"
            :disabled="loading"
            class="w-full bg-black text-white py-4 rounded-xl font-medium hover:opacity-90 transition disabled:opacity-50"
        >
          {{ loading ? 'Enviando...' : 'Enviar mensaje' }}
        </button>

        <p
            v-if="success"
            class="text-green-600 text-center"
        >
          Mensaje enviado correctamente.
        </p>

        <p
            v-if="error"
            class="text-red-500 text-center"
        >
          {{ error }}
        </p>

      </form>

    </div>

  </section>

</template>

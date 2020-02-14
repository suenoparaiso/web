<template>
  <form name="contact" method="post" data-netlify="true" data-netlify-honeypot="bot-field" @submit.prevent="handleSubmit">
    <!-- Name -->
    <div class="field">
      <label class="label is-medium">Nombre</label>
      <div class="control has-icons-left">
        <input class="input is-medium" type="text" name="name" placeholder="Juan Smith" />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="user" />
        </span>
      </div>
    </div>
    <!-- Email -->
    <div class="field">
      <label class="label is-medium">Email</label>
      <div class="control has-icons-left">
        <input class="input is-medium" type="email" name="email" placeholder="tu@email.com" />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="envelope" />
        </span>
      </div>
    </div>
    <!-- Subject -->
    <div class="field">
      <label class="label is-medium">Asunto</label>
      <div class="control has-icons-left">
        <input
          class="input is-medium"
          type="text"
          name="subject"
          placeholder="Asunto de tu mensaje"
        />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="briefcase" />
        </span>
      </div>
    </div>
    <!-- Message -->
    <div class="field">
      <label class="label is-medium">Mensaje</label>
      <div class="control">
        <textarea class="textarea" name="message" placeholder="Tu mensaje" rows="8"></textarea>
      </div>
    </div>
    <div class="control">
      <button class="button is-primary" type="submit">Contáctanos</button>
    </div>
  </form>
</template>

<script>
export default {
  data: () => ({
    form: {
      name: '',
      email: '',
      subject: '',
      message: ''
    }
  }),
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          (key) => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join('&')
    },
    handleSubmit() {
      const axiosConfig = {
        header: { 'Content-Type': 'application/x-www-form-urlencoded' }
      }
      axios.post(
        '/',
        this.encode({
          'form-name': 'contacto',
          ...this.form
        }),
        axiosConfig
      )
    }
  }
}
</script>
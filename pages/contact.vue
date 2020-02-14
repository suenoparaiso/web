<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="Contáctanos & Vistítanos"
      subtitle="Contact & Come Visit Us"
      image="/uploads/planetario-purace.jpg"
    ></site-hero>
    <main-section theme="sidebar-left">
      <template v-slot:default>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <contact-form />
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <p class="title">Visitanos!</p>
        <p class="subtitle">Come visit us!</p>
        <figure class="image is-1by1">
          <opti-image
            :src="require('~/assets/uploads/contact.jpeg').src"
            :srcset="
                    require('~/assets/uploads/contact.jpeg').srcSet
                  "
          />
        </figure>
        <br />
        <div class="content">
          <iframe
            width="100%"
            height="500"
            frameborder="0"
            style="border:0"
            src="https://www.google.com/maps/embed/v1/place?q=place_id:ChIJz_Qa_ZAdMI4RPqb1aGxfhK0&key=AIzaSyDAeYfDzayZFHY7vu0MoYtYReIiqAsPYRo"
            allowfullscreen
          ></iframe>
          <p>Estamos ubicados en el Municipio de Popayán, corregimiento de Cajete. Vereda Santa Ana, Finca Sueño Paraiso.</p>
        </div>
        <div class="content">
          <p>
            <a
              class="button is-primary"
              target="_blank"
              href="https://wa.me/573154183005?text=Hola!%20estoy%20interesadx%20en%20el%20EcoDestino%20"
            >
              Escríbenos por WhatsApp
            </a>
            <br />+573154183005
          </p>
        </div>
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contáctanos | ${this.$siteConfig.siteName}`,
      description: `Como llegar al Eco-Destino`
    }
  },
  components: { ContactForm }
}
</script>

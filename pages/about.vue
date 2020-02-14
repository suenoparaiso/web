<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="EcoDestino Sueño Paraiso"
      subtitle="Acerca de Nosotros | About Us"
      image="/uploads/about-hero.jpeg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>EcoDestino Sueño Paraiso</h3>
          <p>
            <strong>Somos El Ecodestino Sueño Paraiso, una entidad que se proyecta en la ciudad de Popayán, como la mejor oportunidad para vivenciar el contacto con la Tierra y el Universo, a través de la protección del ambiente, el Bienestar integral y el conocimiento astronómico.</strong>
          </p>

          <p>Se trata de un centro educativo en el campo, impactando favorablemente en la calidad de vida de las comunidades, como alternativa al cambio climático planetario.</p>

          <h3>ASESORIA Y CONSULTORIAS EN TURISMO DE NATURALEZA.</h3>
          <p>Se realiza asesoría y consultoría con el fin de fortalecer los procesos de Turismo de Naturaleza en el departamento del Cauca.</p>
          <ul>
            <li>Inventarios y diagnósticos de ofertas turísticas locales y regionales.</li>
            <li>Planes de desarrollo turístico departamental, municipal y local</li>
            <li>Sensibilización en Turismo amigable con la naturaleza.</li>
            <li>Capacitación en: conceptos básicos de: turismo comunitario de naturaleza, agroturismo, aviturismo, senderos ecológicos, interpretación ambiental, bioconstrucción, agricultura orgánica y comida saludable, Giras y experiencias de intercambio de saberes.</li>
            <li>Diseño y costeo de productos turístico, Marketing turístico. Formulación y acompañamiento en proyectos de desarrollo turístico sostenibles,</li>
          </ul>
          <!--<quote-card />-->
          <h3>PLANETARIO MOVIL</h3>
          <p>
            Domo portátil inflable de 4 metros de diámetro x 3 metros de alto, con un sistema de visualización digital que permite recorrer el universo, las galaxias, los sistemas solares, los planetas, la tierra y los diferentes escenarios del planeta mediante sensaciones extraordinarias. Esta experiencia itinerante es una poderosa herramienta divulgativa, pues puede desplazarse a distintos lugares, municipios y ciudades, brindando el conocimiento esencial para generar alternativas de bienestar integral para la comunidad Caucana.
            <strong>Se busca partir desde una exploración del Cosmos hasta su SER</strong>,
            con el fin de despertar el interés y brindar alternativas que amplíen la visión y relación con la vida misma de quienes participen de esta experiencia. A través de los siguientes métodos y contenidos.
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">ESCUELA SEMILLEROS DEL COSMOS CURSO DE ASTRONOMIA</p>
              <p
                class="subtitle"
              >Fortalecer el talento de niños y jóvenes, mediante la formación de líderes ambientales, por medio del aprender haciendo, generando respeto con al entorno ambiental y social.</p>
              <figure class="image is-1by1">
                <opti-image
                  :src="require('~/assets/uploads/semilleros-cosmos.jpeg').src"
                  :srcset="
                    require('~/assets/uploads/semilleros-cosmos.jpeg').srcSet
                  "
                />
              </figure>
            </article>
          </div>
        </div>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">RECORRIDO POR EL SENDERO</p>
              <p
                class="subtitle"
              >Orientado a conocer los diversos ecosistemas que componen la naturaleza y compartiendo con los visitantes, alternativas para asumir responsabilidad frente al cambio climático.</p>
            </article>
          </div>
        </div>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">TALLERES DE BIENESTAR INTEGRAL</p>
              <p
                class="subtitle">
                Desarrollar capacidades que conduzcan a un mejor estilo de vida, por medio de: Talleres de vida saludable, agricultura orgánica, gastronomía, prácticas físico-mental-emocional y espiritual como Yoga, Meditación y Respiración.
                Actividades para docentes, padres de familia, público en general y Turistas.  Pasadía 
              </p>
            </article>
          </div>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">Latest Posts</h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>

<style scoped>
.title{
  font-weight: initial!important;
}
</style>
<template>
  <div id="planetario-movil-page" class="page-wrapper planetario-movil-page content-page">
    <site-hero
      title="Planetario Móvil"
      subtitle="El cosmos en un globo!"
      image="/uploads/planetario-movil-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Planetario Móvil</h3>
          <p>
            <strong>El cosmos en un globo!</strong>
          </p>
          <p>
            Brinda una experiencia de formación única, innovadora y divertida de
            los aspectos del universo y la naturaleza.
          </p>

          <h3>Metodología</h3>
          <p>
            Se utiliza un planetario móvil inflable que servirá como herramienta de formación y motivación a través de temáticas relacionadas con la astronomía y el ambiente.
            <br />El Planetario se instala en el lugar de destino con previa programación.
            <br />Se elige por parte del interesado las temáticas a tratar y se desarrollan las jornadas que pueden ser Una cada mes o una cada semana o una cada día como se prefiera.
            <br />A través de los siguientes métodos.
          </p>
          <ul>
            <li>Talleres participativos.</li>
            <li>Videos sobre la temática tratada.</li>
            <li>Manualidades.</li>
            <li>Trabajo en grupo.</li>
          </ul>
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
      title: `planetario-movil | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>

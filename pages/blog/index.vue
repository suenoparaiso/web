<template>
  <div id="categories-page" class="page-wrapper categories-page">
    <site-hero title="Categories" image="/uploads/contact.jpeg" />
    <main-section theme="one-column">
      <categories-grid />
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Blog | ${this.$siteConfig.siteName}`
    }
  }
}
</script>

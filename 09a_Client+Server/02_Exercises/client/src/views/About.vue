<template>
  <div class="about">
    <h1>ABOUT US </h1>
    <!--
  Vue Directives: Basic Directives (v-text, v-once, v-html, v-bind, v-if, v-show)
  -->
    <div>
      <h1 v-if="true" v-text="text">Loading...</h1>
      <h2 v-else-if="true" v-html="html" />
      <a
          v-else
          :href="link.url"
          :target="link.target"
          :tabindex="link.tabindex"
          v-text="link.title"
      />
    </div>

  </div>
</template>


<script>
export default {
  data() {
    return {
      // v-text
      text: 'Entdecke mehr Produkte...',
      // v-html
      html: 'Andere Beautyprodukte findest du auf unsere Hauptseite: Sephora.com',
      // v-bind
      link: {
        url: 'https://www.sephora.com/',
        target: '_blank',
        tabindex: '0',
        title: 'Hier geht es zur offiziellen Sephora Seite',
      },
    }
  },
}
</script>
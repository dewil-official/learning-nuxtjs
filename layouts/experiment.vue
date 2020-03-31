<template>
  <v-app dark>
    <v-app-bar color="blue" dark app>
      <v-btn icon to="/">
        <v-icon>mdi-chevron-left</v-icon>
      </v-btn>
      <v-toolbar-title>NuxtJS Experiment</v-toolbar-title>
    </v-app-bar>
    <v-content>
      <nuxt />
    </v-content>
  </v-app>
</template>

<script>
export default {
  layout: 'experiment'
}
</script>
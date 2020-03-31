<template>
  <v-list shaped>
    <v-subheader>Experiments 🧪</v-subheader>
    <v-list-item-group v-model="experimentPages" color="primary">
      <v-list-item v-for="(item, i) in experimentPages" :key="i" :to="item.path">
        <v-list-item-icon>
          <v-icon color="blue">mdi-test-tube</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title v-text="item.name"></v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list-item-group>
  </v-list>
</template>

<script>
export default {
  data: () => ({
    experimentPages: []
  }),
  created() {
    this.$router.options.routes.forEach(routeOption => {
      if (routeOption.path.startsWith('/experiments')) {
        this.experimentPages.push({
          name: routeOption.name,
          path: routeOption.path
        })
      }
    })
  }
}
</script>

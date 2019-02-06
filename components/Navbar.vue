<template>
  <v-toolbar dark color="purple">
    <v-toolbar-side-icon />
    <v-toolbar-title>iTunes Search</v-toolbar-title>
    <v-spacer />
    <v-btn icon>
      <nuxt-link to="/" class="ref">
        <v-icon>refresh</v-icon>
      </nuxt-link>
    </v-btn>
  </v-toolbar>
</template>

<script>
export default {

}
</script>

<style scoped>
  .ref {
    text-decoration: none;
    color: white;
  }
</style>

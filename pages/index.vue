<template>
  <v-container grid-list-xs>
    <v-layout row wrap>
      <v-flex xs12>
        <v-form @submit.prevent="searchName">
          <v-text-field
            v-model="name"
            label="Input Artist Name"
            color="purple"
            prepend-inner-icon="person"
          />
        </v-form>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'home | iTunes',
      meta: [
        { name: 'description', content: 'nuxt.js simple API' },
        { name: 'keywords', content: 'itunes, vue.js, nuxt.js, vuetify' }
      ]
    }
  },
  data() {
    return {
      name: ''
    }
  },
  methods: {
    searchName() {
      this.$router.push(`/${this.name}`)
    }
  }
}
</script>

<style>

</style>

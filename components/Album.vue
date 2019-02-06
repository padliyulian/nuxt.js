<template>
  <div
    id="e3"
    style="max-width: 400px; margin: auto;"
    class="grey lighten-3"
  >
    <v-card class="mb-3">
      <v-container
        fluid
        grid-list-lg
      >
        <v-layout row wrap>
          <v-flex xs12>
            <v-card target="_blank" :href="url" :color="color" class="white--text">
              <v-layout row>
                <v-flex xs7>
                  <v-card-title primary-title>
                    <div>
                      <div class="headline">
                        {{ title }}
                      </div>
                      <div>{{ artist }}</div>
                      <div>(2013)</div>
                    </div>
                  </v-card-title>
                </v-flex>
                <v-flex xs5>
                  <v-img
                    :src="image"
                    height="100px"
                    contain
                  />
                </v-flex>
              </v-layout>
              <v-divider light />
              <v-card-actions class="pa-3">
                Rate this album
                <v-spacer />
                <v-icon color="yellow">
                  star_border
                </v-icon>
                <v-icon color="yellow">
                  star_border
                </v-icon>
                <v-icon color="yellow">
                  star_border
                </v-icon>
                <v-icon color="yellow">
                  star_border
                </v-icon>
                <v-icon>star_border</v-icon>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
      default: 'no data'
    },
    image: {
      type: String,
      required: false,
      default: 'no data'
    },
    artist: {
      type: String,
      required: false,
      default: 'no data'
    },
    url: {
      type: String,
      required: false,
      default: 'no data'
    },
    color: {
      type: String,
      required: false,
      default: 'no data'
    }
  }
}
</script>

<style>

</style>

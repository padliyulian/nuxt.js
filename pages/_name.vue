<template>
  <div>
    <h2 class="purple--text my-4 text-xs-center">
      Result Of {{ $route.params.name }}
    </h2>
    <div v-if="cekAlbum">
      <div v-for="(album, index) in resAlbums" :key="album.collectionId">
        <Album
          :title="album.collectionCensoredName"
          :image="album.artworkUrl100"
          :artist="album.artistName"
          :url="album.artistViewUrl"
          :color="getColor(index)"
        />
      </div>
    </div>
    <div v-else>
      <p class="purple--text text-xs-center">
        Albums Doesn't Exsist
      </p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Album from '@/components/Album'

export default {
  components: {
    Album
  },
  head() {
    return {
      title: 'home | iTunes',
      meta: [
        { name: 'description', content: 'nuxt.js simple API' },
        { name: 'keywords', content: 'itunes, vue.js, nuxt.js, vuetify' }
      ]
    }
  },
  asyncData({ params }) {
    return axios.get(`https://itunes.apple.com/search?term=${params.name}&entity=album`)
      .then((res) => {
        return { resAlbums: res.data.results }
      })
  },
  computed: {
    cekAlbum() {
      return this.resAlbums.length > 0
    }
  },
  methods: {
    getColor(index) {
      return index % 2 === 0 ? 'purple' : 'red'
    }
  }
}
</script>

<style>

</style>

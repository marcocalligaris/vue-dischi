<template>
  <div>
    <body>
      <BaseHeader 
      :albums="albums" 
      :genres-options="genresOptions" 
      @genre-change="setSelectedGenre"
      />
      <BaseMain 
      :albums="albums" 
      :selected-genre="selectedGen"
      />
    </body>
  </div>
</template>

<script>
  import BaseHeader from './components/BaseHeader.vue';
  import BaseMain from './components/BaseMain.vue';
  import axios from 'axios';
  export default {
    name: 'App',
    components: {
      BaseHeader,
      BaseMain,
    },
    data() {
          return {
              albums: [],
              selectedGenre: '',
              genresOptions: ['Rock', 'Pop', 'Metal'],
          };
    },
    props: {
      selectedGen: String,
    },
    methods: {
      setSelectedGenre(genre) {
        this.selectedGenre = genre;
      },
      getGenresList() {
        const genres = []
        this.albums.forEach((album) => {
          if(!genres.includes(album.genre)) genres.push(album.genre);
        });
        console.log(genres);
      },
    },
    mounted() {
      axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.albums = res.data.response;
      });
    }
  }
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
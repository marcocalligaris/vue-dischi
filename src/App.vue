<template>
  <div>
    <body>
      <BaseHeader />
      <BaseMain :albums="albums" />
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
            albums: []
        };
    },
    mounted() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
                this.albums = res.data.response;
        });
    },
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
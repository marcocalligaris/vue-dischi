<template>
    <div class="container">
        <div class=" albums-list row py-3 gy-3">
            <div
            v-for="album in albums"
            :key="album.i"
            class="column"
            >
                <AlbumCard
                :image="album['poster']"
                :title="album['title']"
                :author="album['author']"
                :year="album['year']"
                />
            </div>
        </div>
    </div>
</template>
    
<script>
    import axios from 'axios';
    import AlbumCard from './AlbumCard.vue';
    export default {
    name: "AlbumsSection",
    components: { AlbumCard },
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

<style lang="scss" scoped>
    .column {
        width: 20%;
    }
</style>
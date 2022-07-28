<template>
    <div class="container">
        <div class=" albums-list row py-3 gy-3">
            <div
            v-for="album in filteredAlbums"
            :key="album.i"
            class="column"
            >
                <AlbumCard
                :albums="albums"
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
import AlbumCard from './AlbumCard.vue';
export default {
    name: "AlbumsSection",
    components: { AlbumCard }, 
    props: {
        albums: Array,
        selectedGen: String,
    },
    computed: {
        filteredAlbums() {
            if(!this.selectedGen) return this.albums;
            return this.albums.filter((album) => album.genre === this.selectedGen);
            },
    },
}
</script>

<style lang="scss" scoped>
    .column {
        width: 20%;
    }
</style>
<template>
    <div class="container">
        <div class=" albums-list row gy-3">
            <div class="col-2" v-for="album in albums" :key="album.i">{{album.title}}</div>
        </div>
    </div>
</template>
    
<script>
    import axios from 'axios';
    export default {
        name: 'AlbumsSection',
        data(){return {
            albums: []
        }},
        mounted(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res) =>{
                this.albums = res.data.response;
            });
        }
    }
</script>

<style lang="scss" scoped>
</style>
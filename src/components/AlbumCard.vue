<template>
    <div class="album-card p-3 text-center">
        <img :src="image" alt="title" class="img-fluid mb-3">
        <h3>{{title}}</h3>
        <h5>{{author}}</h5>
        <p>{{year}}</p>
    </div>
</template>

<script>
export default {
    name: 'AlbumCard',
    props: {
        author: String,
        image: String,
        title: String,
        year: String,
    }
}
</script>
<style lang="scss" scoped>
    @import '../assets/scss/vars';
    .album-card {
        background-color: $grey;
        height: 450px;
        h3 {
            color: white;
        }
        h5, p {
            color: grey;
        }
    }
</style>
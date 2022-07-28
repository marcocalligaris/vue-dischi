<template>
    <main>
        <section id="albums">            
            <AlbumsSection :albums="albums" :selectedGen="selectedGen" />
        </section>
    </main>
</template>

<script>
import AlbumsSection from './AlbumsSection.vue';
export default {
    name: "BaseMain",
    props: {
        albums: Array,
        selectedGen: String,
    },
    components: { AlbumsSection }
}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/vars';
    main {
        height: auto;
    }
</style>
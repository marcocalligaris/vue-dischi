<template>
    <main>
        <section id="albums">            
            <AlbumsSection />
        </section>
    </main>
</template>

<script>
import AlbumsSection from './AlbumsSection.vue';
export default {
    name: "BaseMain",
    components: { AlbumsSection }
}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/vars';
    main {
        background-color: $dark_grey;
        height: auto;
    }
</style>
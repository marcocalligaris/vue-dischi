<template>
    <nav class=" px-4 d-flex justify-content-between align-items-center">
        <BaseLogo />
        <BaseSelect placeholder="Seleziona Genere" :options="genresOptions" @option-change="emitGenreChange" />
    </nav>
</template>

<script>
    import BaseLogo from '../components/BaseLogo.vue';
    import BaseSelect from '../components/BaseSelect.vue';
    export default {
        name: 'BaseHeader',
        components: {
            BaseLogo,
            BaseSelect,
        },
        props: {
            genresOptions: Array,
        },
        methods: {
            emitGenreChange(genre) {
                this.$emit('genre-change', genre);
            },
        }
    };
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';
nav {
    background-color: $grey;
    width: 100%;
    height: 80px;
    }
</style>
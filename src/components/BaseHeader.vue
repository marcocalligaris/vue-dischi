<template>
    <header class="py-2 px-4">
        <nav class="d-flex align-items-center">
            <BaseLogo />
        </nav>
    </header>
</template>

<script>
    import BaseLogo from '../components/BaseLogo.vue';
    export default {
        name: 'BaseHeader',
        components: {
            BaseLogo,
        }
    }
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';
header {
    background-color: $grey;
    width: 100%;
}
</style>
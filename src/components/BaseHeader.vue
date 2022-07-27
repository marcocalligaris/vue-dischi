<template>
    <div class="d-flex align-items-center py-2 px-4 ">
            <BaseLogo />
    </div>
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
div {
    background-color: $grey;
    width: 100%;
    height: 80px;
    }
</style>
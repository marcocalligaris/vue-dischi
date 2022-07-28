<template>
    <nav class=" px-4 d-flex justify-content-between align-items-center">
        <div class="d-flex align-items-center">
            <BaseLogo />
        </div>
        <BaseSelect />
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
        }
    }
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';
nav {
    background-color: $grey;
    width: 100%;
    height: 80px;
    }
</style>
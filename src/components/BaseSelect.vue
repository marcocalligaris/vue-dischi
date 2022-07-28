<template>
    <select class="form-select form-select-sm">
        <option selected>Open this select menu</option>
        <option value="1">One</option>
        <option value="2">Two</option>
        <option value="3">Three</option>
    </select>
</template>

<script>
export default {
    name: 'BaseSelect',
}
</script>

<style lang="scss" scoped>
    select {
        width: 300px;
    }
</style>
<template>
<div>
    <select 
        class="form-select form-select-sm" v-model="selectedOption" @change="emitChange">
        <option 
        value="">{{ placeholder || 'Select an option' }}</option>
        <option 
        v-for="option in options" 
        :key="option.value || option" 
        :value="option.value || option"
        >
        {{ option.label || option }}
        </option>
    </select>
</div>
</template>

<script>
    export default {
        name: 'BaseSelect',
            data() {
                return {
                    selectedOption: ''
                };
            },
        props: {
            placeholder: String,
            options: Array,
        },
        methods: {
            emitChange() {
                this.$emit('option-change', this.selectedOption);
            }
        },
    }
</script>
<template>
    <input :value="modelValue" @input="updateInput" class="input_form">
</template>

<script>
export default {
    name: 'my-input',

    props: {
        modelValue: [String, Number],
    },

    methods: {
        updateInput(event){
            this.$emit('update:modelValue', event.target.value);
        }
    }
}
</script>

<style>
.input_form {
    width: 100%;
    border: 2px solid #002c85;
    padding: 10px 15px;
    margin-top: 15px;
}
</style>
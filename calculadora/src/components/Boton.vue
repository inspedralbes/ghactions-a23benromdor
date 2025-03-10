<script setup>
const props = defineProps({
    numero: {
        type: Number,
        required: true
    }
});
</script>

<template>
    <button>{{ numero }}</button>
</template>

<style scoped>
</style>
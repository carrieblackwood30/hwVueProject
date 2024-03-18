<template>
    <button>{{ next }}</button>
</template>

<script setup>
defineProps({
    next: String
})
</script>

<style>
button {
    background-color: #4646dc;
    color: aliceblue;
    padding: .5rem 1rem;
    border-radius: 10px;
}
</style>
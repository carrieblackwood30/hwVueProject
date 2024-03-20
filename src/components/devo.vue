<template>
    <div>{{ card }}
        <h3>{{ title }}</h3>
        <p>{{ cost }}</p>
        <button>{{ addCostBtn }}</button>
    </div>

</template>

<script setup>
defineProps({
    card: '',
    title: String,
    cost: Number,
    addCostBtn: String
})
</script>

<style scoped>
button {
    background-color: #4646dc;
    color: aliceblue;
    padding: .5rem 1rem;
    border-radius: 10px;
}

div {
    border: 1px solid black;
    border-radius: 10px;
    width: fit-content;
}

template {
    display: flex;
}
</style>
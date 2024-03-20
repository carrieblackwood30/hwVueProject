<template>

  <div class="cards">
    <div v-for="item in items" :key="item">
      <h4>{{ item.name }}</h4>
      <p>{{ item.cost }}</p>
      <button @click="plus(item)">{{ item.button }}</button>
    </div>
  </div>

  <h3>cost is:{{ num }}</h3>

</template>

<script setup>
import { computed, reactive, ref } from 'vue';

let num = ref(0)

const items = reactive([
  {
    name: "Iphone",
    cost: 1000,
    button: "add item"
  },
  {
    name: "macbook",
    cost: 3000,
    button: "add item"
  },
  {
    name: "watch",
    cost: 200,
    button: "add item"
  }
])

const plus = (item) => {
  console.log(`${item.name}`)

  const compPlus = computed(
    num.value = num.value + item.cost
  )
  console.log(compPlus)
  return compPlus
}

</script>

<style scoped>
.cards {
  display: flex;
  gap: 1rem;
}

.cards div {
  border: 1px solid black;
  padding: 1rem;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
}
</style>
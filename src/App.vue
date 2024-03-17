<template>

  <button @click="createImg">add card</button><br>

  <div v-for="img in cards">
    <img v-bind:src="img" width="100%" height="100%">
  </div>

</template>

<script setup>
import { ref } from 'vue';

const cards = ref([])

function createImg() {
  let newImg = prompt("add a link of image")
  let checkEnd = newImg.split('.')
  console.log(checkEnd[checkEnd.length - 1])
  if (newImg !== '') {
    if (checkEnd[checkEnd.length - 1] === 'jpg' || checkEnd[checkEnd.length - 1] === 'png' || checkEnd[checkEnd.length - 1] === 'jpeg') {
      cards.value.push(newImg)
    }
    else (alert('ссылка должна быть на изображение'))
  } else (alert('поле пустое!'))
}

</script>

<style scoped>
div {
  border: 1px solid;
  width: fit-content;
  border-radius: 10px;
  display: inline-block;
  margin: 2rem;
  padding: 1rem;
  object-fit: contain;
  width: 200px;
}
</style>
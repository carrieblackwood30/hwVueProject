<template>
  <img :src="hokage[sum]" alt="hokages" width="400"><br>
  <devo next="prev" @click="prev"></devo>
  <button @click="next">next</button>
</template>

<script setup>
import { reactive, ref } from 'vue';
import devo from './components/devo.vue';
const hokage = reactive([
  "https://wallpaperaccess.com/full/5848355.png",
  "https://i.ytimg.com/vi/kqr2QuM8XXo/maxresdefault.jpg?sqp=-oaymwEmCIAKENAF8quKqQMa8AEB-AHmCYAC0AWKAgwIABABGGUgWyhNMA8=&rs=AOn4CLD5XJcAaRoihjKonmJpLfNtRNgBEg",
  "https://static0.gamerantimages.com/wordpress/wp-content/uploads/2022/08/Collage-Maker-08-Aug-2022-0650-AM.jpg",
  "https://wallpapers.com/images/hd/fourth-hokage-1280-x-936-wallpaper-vspp9piq5py2nbim.jpg",
  "https://i.ytimg.com/vi/5v92hLp9OAI/maxresdefault.jpg"
])
let sum = ref(0)
let next = () => sum.value > hokage.length - 2 ? sum.value = 0 : sum.value += 1
let prev = () => sum.value < 1 ? sum.value = hokage.length - 1 : sum.value -= 1
</script>
<template>
  <div id="gifList">
    <gif v-for="gif in gifs" :gif="gif" :key="gif.id"/>
  </div>
</template>

<script>
import Gif from "@/components/Gif";
export default {
name: "GifList",
  components: {Gif},
  props: ['gifs']
}
</script>

<style scoped>
  #gifList {
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
</style>
<template>
    <search-input @gifs-fetched="onGifsFetched"/>

    <gif-list :gifs="gifs"/>
</template>

<script>

import SearchInput from "@/components/SearchInput";
import GifList from "@/components/GifList";

export default {
  name: 'App',
  components: {
    GifList,
    SearchInput
  },
  data() {
    return {
      gifs: [],
    }
  },
  methods: {
    onGifsFetched(result) {
      console.log(result);
      this.gifs = result.data
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
body {
  padding: 50px
}

#app {
  width: 800px;
  margin: 0 auto;
}
</style>

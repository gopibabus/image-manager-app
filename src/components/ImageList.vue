<template>
<div>
  <div v-if="isLoggedIn" class="image-container">
   <img :key="image.link" v-for="image in allImages" :src="image.link"/>
  </div>
  <h2 v-else>
    Login in to get started!!
  </h2>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: 'ImageList',
  methods: mapActions(['fetchImages']),
  computed: mapGetters(['allImages', 'isLoggedIn']),
  created(){
    if(this.isLoggedIn){
      this.fetchImages();
    }
  }
}
</script>

<style scoped>
.image-container {
  column-count: 3;
  column-gap: 0;
}

img {
  max-width: 100%;
  padding: 5px;
}
</style>

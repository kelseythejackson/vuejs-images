<template>
  <div>
    Image List
    <img v-for="image in allImages" :key="image.id" :src="image.link" alt="image.description">
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex'
export default {
  name: 'ImageList',
  computed: mapGetters(['allImages']),
  methods: mapActions(['fetchImages']),
  created() {
    this.fetchImages()
  }
};
</script>

<style scoped></style>

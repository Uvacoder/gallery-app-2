<template>
  <div>
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <ul>
      <li
        v-for="(thumb, thumbIndex) in [
          'swood.jpg',
          'swood.jpg',
        ]"
        :key="thumbIndex"
        @click="index = thumbIndex"
      >
        <img :src="thumb">
      </li>
    </ul>
  </div>
</template>

<script>
import Vue from 'vue';
  import { LightGallery } from 'vue-light-gallery';

  export default {
    components: {
      LightGallery,
    },
    data() {
      return {
        images: [
          { title:'img 1', url: 'swood.jpg' },
          { title:'img 2', url: 'swood.jpg' },
        ],
        index: null,
      };
    },
  };
</script>
<style scoped>
.light-gallery__close {
    margin-top: 5em;
}
</style>
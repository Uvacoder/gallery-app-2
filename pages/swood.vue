<template>
  <div class="container">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <ul>
      <li
        v-for="(thumb, thumbIndex) in [
          '/swood/swood01-150x150.jpg',
          '/swood/swood02-150x150.jpg',
          '/swood/swood03-150x150.jpg',
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
          { title:'img 1', url: '/swood/swood01.jpg' },
          { title:'img 2', url: '/swood/swood02.jpg' },
          { title:'img 3', url: '/swood/swood02.jpg' },
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

ul {
  list-style: none;
  padding: 0;
  margin-top: 40px;
  display: inline-grid;
  grid-template-columns: auto auto auto;
  grid-column-gap: 20px;
  justify-content: space-evenly;
}

</style>
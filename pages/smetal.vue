<template>
  <div class="container">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <h3>Sculptures - Metal</h3>
    <ul>
      <li
        v-for="(thumb, thumbIndex) in [
            '/smetal/smetal01-150x150.jpg',
            '/smetal/smetal02-150x150.jpg',
            '/smetal/smetal03-150x150.jpg',
            '/smetal/smetal04-150x150.jpg',
            '/smetal/smetal05-150x150.jpg',
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
            { title:'Autumn (12" x 9.5" x 8")', url: '/smetal/smetal01.jpg' },
            { title:'Late Autumn (12" x 12" x 22")', url: '/smetal/smetal02.jpg' },
            { title:'After All (20" x 13" x 11")', url: '/smetal/smetal03.jpg' },
            { title:'Went By (8" x 4" x 12")', url: '/smetal/smetal04.jpg' },
            { title:'Inevitable (11" x 11" x 21")', url: '/smetal/smetal05.jpg' },
        ],
        index: null,
      };
    },
  };
</script>
<style scoped>
  h3 {
    margin: 30px 15px 0 15px;
  }

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
    grid-row-gap: 15px;
    justify-content: space-evenly;
  }

  img {
      border: 1px solid #666;
  }
</style>
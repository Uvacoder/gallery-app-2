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
            '/sorganic/sorganic01-150x150.jpg',
            '/sorganic/sorganic02-150x150.jpg',
            '/sorganic/sorganic03-150x150.jpg',
            '/sorganic/sorganic04-150x150.jpg',
            '/sorganic/sorganic05-150x150.jpg',
            '/sorganic/sorganic06-150x150.jpg',
            '/sorganic/sorganic07-150x150.jpg',
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
            { title:'Love Me Tender (12" x 12" x 18")', url: '/sorganic/sorganic01.jpg' },
            { title:'Growing (26" x 13" x 13")', url: '/sorganic/sorganic02.jpg' },
            { title:'Incubation (25" x 15" x 20")', url: '/sorganic/sorganic03.jpg' },
            { title:'Fruition (16" x 13" x 13")', url: '/sorganic/sorganic04.jpg' },
            { title:'Echo (22" x 12" x 12")', url: '/sorganic/sorganic05.jpg' },
            { title:'Inception (20" x 10" x 10")', url: '/sorganic/sorganic06.jpg' },
            { title:'Untitled (34" x 12" x 12")', url: '/sorganic/sorganic07.jpg' },
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

  div {
      font-size: 12px !important;
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
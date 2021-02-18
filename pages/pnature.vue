<template>
  <div class="container box">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <h3>Paintings - Nature</h3>
    <ul class="display">
      <li
        v-for="(thumb, thumbIndex) in [
            '/pnature/pnature01-150x150.jpg',
            '/pnature/pnature02-150x150.jpg',
            '/pnature/pnature03-150x150.jpg',
            '/pnature/pnature04-150x150.jpg',
            '/pnature/pnature05-150x150.jpg',
            '/pnature/pnature06-150x150.jpg',
            '/pnature/pnature07-150x150.jpg',
            '/pnature/pnature08-150x150.jpg',
            '/pnature/pnature09-150x150.jpg',
            '/pnature/pnature10-150x150.jpg',
            '/pnature/pnature11-150x150.jpg',
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
  import { LightGallery } from 'vue-light-gallery';

  export default {
    components: {
      LightGallery,
    },
    data() {
      return {
        images: [
            { title:'Abundance (11" x 13.5", Monotype)', url: '/pnature/pnature01.jpg' },
            { title:'Pears (23" x 17", Monotype)', url: '/pnature/pnature02.jpg' },
            { title:'Tropicana (50" x 38", Oil Painting)', url: '/pnature/pnature03.jpg' },
            { title:'Tulips (11" x 13", Monotype)', url: '/pnature/pnature04.jpg' },
            { title:'Iris (11" x 13.5", Monotype)', url: '/pnature/pnature05.jpg' },
            { title:'Lilies I (11" x 13.5", Monotype)', url: '/pnature/pnature06.jpg' },
            { title:'Lilies II (11" x 13.5", Monotype)', url: '/pnature/pnature07.jpg' },
            { title:'Cotton Candies (11" x 13.5", Monotype)', url: '/pnature/pnature08.jpg' },
            { title:'Poppies (11" x 13.5", Monotype)', url: '/pnature/pnature09.jpg' },
            { title:'Roses (11" x 13.5", Monotype)', url: '/pnature/pnature10.jpg' },
            { title:'Creek (11" x 13.5", Monotype)', url: '/pnature/pnature11.jpg' },
        ],
        index: null,
      };
    },
  };
</script>
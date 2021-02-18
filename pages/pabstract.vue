<template>
  <div class="container box">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <h3>Paintings - Abstract</h3>
    <ul class="display">
      <li
        v-for="(thumb, thumbIndex) in [
          '/pabstract/pabstract01-150x150.jpg',
          '/pabstract/pabstract02-150x150.jpg',
          '/pabstract/pabstract03-150x150.jpg',
          '/pabstract/pabstract04-150x150.jpg',
          '/pabstract/pabstract05-150x150.jpg',
          '/pabstract/pabstract06-150x150.jpg',
          '/pabstract/pabstract07-150x150.jpg',
          '/pabstract/pabstract08-150x150.jpg',
          '/pabstract/pabstract09-150x150.jpg',
          '/pabstract/pabstract10-150x150.jpg',
          '/pabstract/pabstract11-150x150.jpg',
          '/pabstract/pabstract12-150x150.jpg',
          '/pabstract/pabstract13-150x150.jpg',
          '/pabstract/pabstract14-150x150.jpg',
          '/pabstract/pabstract15-150x150.jpg',
          '/pabstract/pabstract16-150x150.jpg',
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
          { title:'The Dog and Us (11" x 13.5", Monotype)', url: '/pabstract/pabstract01.jpg' },
          { title:'High Way (23" x 17", Monotype)', url: '/pabstract/pabstract02.jpg' },
          { title:'Path in The Dream (11" x 13.5", Monotype)', url: '/pabstract/pabstract03.jpg' },
          { title:'It’s Happening (11" x 13.5", Monotype)', url: '/pabstract/pabstract04.jpg' },
          { title:'Dancing in The Park (11" x 13", Monotype)', url: '/pabstract/pabstract05.jpg' },
          { title:'The Harbor (11" x 13.5", Monotype)', url: '/pabstract/pabstract06.jpg' },
          { title:'Pink in Africa (23" x 17", Monotype)', url: '/pabstract/pabstract07.jpg' },
          { title:'Surfacing (23" x 17", Monotype)', url: '/pabstract/pabstract08.jpg' },
          { title:'The Spice (11" x 13.5", Monotype)', url: '/pabstract/pabstract09.jpg' },
          { title:'In The Shadow of The Dawn (23" x 17", Monotype)', url: '/pabstract/pabstract10.jpg' },
          { title:'Falling in Love (11" x 13.5", Monotype)', url: '/pabstract/pabstract11.jpg' },
          { title:'Connected (11" x 13.5", Monotype)', url: '/pabstract/pabstract12.jpg' },
          { title:'Chasing in Forest (11" x 13.5", Monotype)', url: '/pabstract/pabstract13.jpg' },
          { title:'Big Bang (11" x 13.5", Monotype)', url: '/pabstract/pabstract14.jpg' },
          { title:'Landing (11" x 13.5", Monotype)', url: '/pabstract/pabstract15.jpg' },
          { title:'Time (65" x 35", Oil Painting)', url: '/pabstract/pabstract16.jpg' },
        ],
        index: null,
      };
    },
  };
</script>
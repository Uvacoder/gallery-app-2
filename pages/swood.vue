<template>
  <div class="container box">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <h3>Sculptures - Wood</h3>
    <ul class="display">
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
  import { LightGallery } from 'vue-light-gallery';

  export default {
    components: {
      LightGallery,
    },
    data() {
      return {
        images: [
          { title:'Setback (7" x 7" x 16")', url: '/swood/swood01.jpg' },
          { title:'Aged (10" x 10" x 12")', url: '/swood/swood02.jpg' },
          { title:'Burnt (18" x 8" x 6")', url: '/swood/swood03.jpg' },
        ],
        index: null,
      };
    },
  };
</script>
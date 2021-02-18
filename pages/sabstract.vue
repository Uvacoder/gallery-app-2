<template>
  <div class="container">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <h3>Sculptures - Abstract</h3>
    <ul>
      <li
        v-for="(thumb, thumbIndex) in [
          '/sabstract/sabstract01-150x150.jpg',
          '/sabstract/sabstract02-150x150.jpg',
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
          { title:'Obsession (20" x 16" x 10")', url: '/sabstract/sabstract01.jpg' },
          { title:'Balancing (N/A)', url: '/sabstract/sabstract02.jpg' },
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
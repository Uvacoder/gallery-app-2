<template>
  <div class="container">
    <LightGallery
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <h3>Paintings - Abstract</h3>
    <ul>
      <li
        v-for="(thumb, thumbIndex) in [
          '/pchickens/pchickens01-150x150.jpg',
          '/pchickens/pchickens02-150x150.jpg',
          '/pchickens/pchickens03-150x150.jpg',
          '/pchickens/pchickens04-150x150.jpg',
          '/pchickens/pchickens05-150x150.jpg',
          '/pchickens/pchickens06-150x150.jpg',
          '/pchickens/pchickens07-150x150.jpg',
          '/pchickens/pchickens08-150x150.jpg',
          '/pchickens/pchickens09-150x150.jpg',
          '/pchickens/pchickens10-150x150.jpg',
          '/pchickens/pchickens11-150x150.jpg',
          '/pchickens/pchickens12-150x150.jpg',
          '/pchickens/pchickens13-150x150.jpg',
          '/pchickens/pchickens14-150x150.jpg',
          '/pchickens/pchickens15-150x150.jpg',
          '/pchickens/pchickens16-150x150.jpg',
          '/pchickens/pchickens17-150x150.jpg',
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
          { title:'Like Father Like Son (23" x 17", Monotype)', url: '/pchickens/pchickens01.jpg' },
          { title:'The King (17" x 23", Monotype)', url: '/pchickens/pchickens02.jpg' },
          { title:'Rock Star (17" x 23", Monotype)', url: '/pchickens/pchickens03.jpg' },
          { title:'Mama’s Boy (17" x 23", Monotype)', url: '/pchickens/pchickens04.jpg' },
          { title:'Ninja (17" x 23", Monotype)', url: '/pchickens/pchickens05.jpg' },
          { title:'The Thinker (23" x 17", Monotype)', url: '/pchickens/pchickens06.jpg' },
          { title:'Napoleon (11" x 13.5", Monotype)', url: '/pchickens/pchickens07.jpg' },
          { title:'Date Night (23" x 17", Monotype)', url: '/pchickens/pchickens08.jpg' },
          { title:'The Boss (17" x 23", Monotype)', url: '/pchickens/pchickens09.jpg' },
          { title:'Trend Setter (16" x 19",, Monotype)', url: '/pchickens/pchickens10.jpg' },
          { title:'Family Time (19" x 16", Monotype)', url: '/pchickens/pchickens11.jpg' },
          { title:'Trouble Makers (23" x 17", Monotype)', url: '/pchickens/pchickens12.jpg' },
          { title:'The Bachelor (17" x 23", Monotype)', url: '/pchickens/pchickens13.jpg' },
          { title:'On A Mission (23" x 17", Monotype)', url: '/pchickens/pchickens14.jpg' },
          { title:'General Tso (17" x 23", Monotype)', url: '/pchickens/pchickens15.jpg' },
          { title:'Good Morning (17" x 23", Monotype)', url: '/pchickens/pchickens16.jpg' },
          { title:'My Angel (17" x 23", Oil Painting)', url: '/pchickens/pchickens17.jpg' },
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
    grid-template-columns: auto auto auto auto auto auto;
    grid-column-gap: 20px;
    grid-row-gap: 15px;
    justify-content: space-evenly;
  }

  img {
    border: 1px solid #666;
  }
</style>
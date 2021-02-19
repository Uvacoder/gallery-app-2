<template>
  <div class="container pt-32">
    <masonry-images/>
  </div>
</template>

<script>
  import MasonryImages from "../components/MasonryImages";

  export default {
    components: {
      MasonryImages,
    }
  }
</script>

<style>
  h3 {
    margin: 30px 15px 8px 0;
  }

  section {
    margin-bottom: 64px;
  }

  .light-gallery__text {
    bottom: -34px !important;
    padding: 12px !important;
    font-size: 12px;
  }

  .light-gallery__close {
    margin-top: 5em;
    right: 1.5% !important;
  }

  .light-gallery__image img {
    max-width: auto !important;
    max-height: 85vh !important;
  }

  .masonry-bottom {
    margin-top: 0 !important;
    padding-top: 0 !important;
    min-height: auto !important;
  }

  .display {
    max-width: 800px;
    list-style: none;
    margin: 40px auto auto 0;
    padding: 0;
    display: grid;
    grid-gap: 2rem;
    grid-template-columns: repeat(auto-fit, minmax(150px, max-content));
  }

  .display li {
      line-height: 0 !important;
      height: 150px !important;
  }

  .display img {
      border: 1px solid #666;
  }

  .box {
    max-width: 1000px;
    padding: 0 2.5rem;
  }

  button {
    width: 80px;
    height: 60px;
  }
</style>

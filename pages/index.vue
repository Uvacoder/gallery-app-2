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

<style lang="less">
  h3 {
    margin-bottom: 8px;
  }

  section {
    margin-bottom: 64px;
  }

  .light-gallery__text {
    bottom: -34px !important;
    font-size: 12px;
  }

  .light-gallery__close {
    margin-top: 5em;
  }

  .masonry-bottom {
    margin-top: 0 !important;
    padding-top: 0 !important;
    min-height: auto !important;
  }
</style>

<template>
  <div class="container pt-32 pb-128">
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
    bottom: -34px;
    font-size: 12px;
  }

  .light-gallery__close {
    margin-top: 5em;
  }
</style>

<template>
  <div class="Header">
    <div class="container h-100 flex-align-center">
      <nuxt-link to="/" class="lh-0 flex-align-center">
        <h2 class="ml-16">
          PaoStudio.Art
        </h2>
      </nuxt-link>
      <div class="flex-grow"/>
      <div class="flex-wrap m--8">
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "NavHeader"
  }
</script>

<style scoped lang="less">
  .Header {
    height: 64px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 10;
    background: #262626;
  }

  a {
    text-decoration: none;
    color: #D43790;
  }

  h2 {
    color: #D43790;
  }
</style>

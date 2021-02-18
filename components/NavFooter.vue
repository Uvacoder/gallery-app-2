<template>
  <nav class="mt-64 pt-40 pb-32">
    <div class="container box">
      <div class="flex-1-2-3 mt-32">
        <div>
          &copy; <nuxt-link to="/about">Pao Hung</nuxt-link>. All Rights Reserved.
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: "NavFooter"
  }
</script>

<style scoped>
  nav {
    background: #fff;
    color: #666;
  }

  a {
    color: #666;
    text-decoration: underline;
  }
</style>

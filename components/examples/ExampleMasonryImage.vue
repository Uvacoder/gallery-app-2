<template>
  <section>
    <vue-masonry-wall :items="items" :options="options" @append="append">
      <template v-slot:default="{item}">
        <nuxt-link :to="`/${item.link}`">
        <div class="Item">
          <img :src="item.image"/>

          <div class="Content">
            <h5 class="text-ellipsis-1l">{{item.title}}</h5>
            <p class="text-ellipsis-2l">{{item.content}}</p>
          </div>
        </div>
        </nuxt-link>
      </template>
    </vue-masonry-wall>
  </section>
</template>

<script>
  import VueMasonryWall from "vue-masonry-wall";

  export default {
    name: "ExampleMasonry",
    components: {VueMasonryWall},
    data() {
      return {
        options: {
          width: 300,
          padding: {
            2: 8,
            default: 12
          },
        },
        items: [
          {
            title: 'Wood Series',
            content: 'Clay Sculptures',
            image: 'swood.jpg',
            link: 'swood'
          },
          {
            title: 'Abstract Forms',
            content: 'Clay Sculptures',
            image: 'pabstract.jpg',
            link: 'pabstract'
          },
          {
            title: 'Organic Forms',
            content: 'Clay Sculptures',
            image: 'sorganic.jpg',
            link: 'sorganic'
          },
          {
            title: 'Metal Series',
            content: 'Clay Sculptures',
            image: 'smetal.jpg',
            link: 'smetal'
          },
          {
            title: 'Nature Series',
            content: 'Paintings',
            image: 'pnature.jpg',
            link: 'pnature'
          },
          {
            title: 'Chicken Series',
            content: 'Paintings',
            image: 'pchickens.jpg',
            link: 'pchicken'
          },
        ]
      }
    }
  }
</script>

<style scoped>
  .Item {
    overflow: hidden;
    border-radius: 4px;
    width: 100%;
    background: #262626;
  }

  .Content {
    padding: 20px;
  }

  h5 {
    color: #D43790;
  }

  p {
    color: #eee;
  }

  img {
    object-fit: cover;
    width: 100%;
    height: 100%;
    line-height: 0;
    display: block;
  }
</style>

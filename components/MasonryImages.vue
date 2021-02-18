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
    name: "MasonryImages",
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
            image: '/swood/swood.jpg',
            link: 'swood'
          },
          {
            title: 'Abstract Forms',
            content: 'Clay Sculptures',
            image: '/sabstract/sabstract.jpg',
            link: 'sabstract'
          },
          {
            title: 'Metal Series',
            content: 'Clay Sculptures',
            image: '/smetal/smetal.jpg',
            link: 'smetal'
          },
          {
            title: 'Organic Forms',
            content: 'Clay Sculptures',
            image: '/sorganic/sorganic.jpg',
            link: 'sorganic'
          },
          {
            title: 'Nature Series',
            content: 'Paintings',
            image: '/pnature/pnature.jpg',
            link: 'pnature'
          },
          {
            title: 'Abstract Forms',
            content: 'Paintings',
            image: '/pabstract/pabstract.jpg',
            link: 'pabstract'
          },
          {
            title: 'Chicken Series',
            content: 'Paintings',
            image: '/pchickens/pchickens.jpg',
            link: 'pchickens'
          }
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

  a {
    text-decoration: none;
  }

  img {
    object-fit: cover;
    width: 100%;
    height: 100%;
    line-height: 0;
    display: block;
  }
</style>

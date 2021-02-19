<template>
  <section>
    <vue-masonry-wall :items="items" :options="options" @append="append">
      <template v-slot:default="{item}">
        <nuxt-link :to="`/${item.link}`">
        <div class="item">
          <img :src="item.image"/>
          <div class="content">
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
  .item {
    overflow: hidden;
    border-radius: 4px;
    width: 100%;
    background: #262626;
  }

  .content {
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

  .masonry-column:nth-child(1) img {
    animation: fade-in 3s 1 ease-in-out forwards;
  }

  .masonry-column:nth-child(2) img {
    animation: fade-in 4s 1 ease-in-out forwards;
  }
  
  .masonry-column:nth-child(3) img {
    animation: fade-in 5s 1 ease-in-out forwards;
  }
  
  .masonry-column:nth-child(4) img {
    animation: fade-in 6s 1 ease-in-out forwards;
  }



@keyframes fade-in {
  0%  { opacity: 0; }
  100% { opacity: 1; } 
}
</style>

<template>
  <bulma-card>
    <div slot="image" class="">
      <figure class="image is-3by2">
        <img class="lazy-img-fadein" v-lazy="movie.field_image.thumbnail.url" v-if="movie.field_image" />
      </figure>
    </div>
    <div slot="content" class="has-text-centered">
      <div class="description">
        <h3 class="title is-5">{{ movie.title }}</h3>
      </div>
    </div>
  </bulma-card>
</template>

<script>
import BulmaCard from '~/components/BulmaCard'
export default {
  components: {
    BulmaCard
  },
  props: {
    movie: { type: Object, default: () => [] }
  },
  data () {
    return {
      imgUrl: 'https://ia.media-imdb.com/images/M/MV5BMjMxNjY2MDU1OV5BMl5BanBnXkFtZTgwNzY1MTUwNTM@._V1_UX182_CR0,0,182,268_AL__QL50.jpg'
    }
  }
}
</script>

<style scoped>

  .thumbnail {
    max-height: 220px;
    overflow: hidden;
  }

  .image.is-square {
    background-color:whitesmoke
  }

  .card:hover {
    transition: all 0.2s ease-in-out;
    top: -10px;
    box-shadow: 0 2px 30px;
  }

  .card {
    height: 100%;
    position: relative;
    transition: all 0.3s ease-in-out;
    top: 0
  }

  .card .description {
    font-style: italic
  }

  .recipes .card .difficulty {
    margin-bottom: 10px;
  }

</style>

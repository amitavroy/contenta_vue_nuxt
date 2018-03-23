<template>
  <div class="recipes">
    <bulma-grid :items="movies" itemsByRow="4">
      <template slot-scope="props">
        <movie-card :movie="props.item" />
      </template>
    </bulma-grid>
  </div>
</template>

<script>
import BulmaGrid from '~/components/BulmaGrid'
import MovieCard from '~/components/movies/MovieCard'
export default {
  components: {
    MovieCard,
    BulmaGrid
  },
  props: {
    movies: {
      type: Array,
      default: () => []
    }
  }
}
</script>

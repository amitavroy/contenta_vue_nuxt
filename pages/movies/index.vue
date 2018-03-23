<template>
  <AppSection>
    <div class="container">
      <h3 class="title is-h3 has-text-centered"> List of movies </h3>
      <!--<pre>{{movies}}</pre>-->
      <movies-list-cards :movies="movies" />
    </div>
  </AppSection>
</template>

<script>
import AppSection from '~/components/AppSection'
import MoviesListCards from '~/components/movies/MoviesListCards'
import {getMovies} from '../../lib/api'
export default {
  components: {
    AppSection,
    MoviesListCards
  },
  async asyncData () {
    let movies = await getMovies()
    return {
      movies
    }
  }
}
</script>

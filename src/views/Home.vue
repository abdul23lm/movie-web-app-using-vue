<template>
  <div class="home">
    <Navbar />

    <div id="main-section">
      <Sidebar />
      <MovieList />
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar'
import Sidebar from '../components/Sidebar'
import MovieList from '../components/MovieList'

export default {
  name: 'Home',
  components: {
    Navbar,
    Sidebar,
    MovieList
  }
}
</script>

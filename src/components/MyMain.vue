<template>
  <div>
    <ul>
      <li>Titolo - lingua - voto</li>

      <li v-for="(film, index) in film_list" :key="index">
        {{film.title}} -
        {{film.original_title}} -
        {{film.original_lenguage}} -
        {{film.vote_avarage}}
      </li>

    </ul>

  </div>
</template>

<script>
export default {
    name:"MyMain",
    props: {
      film_list: Array
    }
}
</script>

<style>

</style>
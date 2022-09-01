<template>
  <div>
    <ul>
      <li>Titolo - lingua - voto</li>

      <li v-for="(film, index) in list" :key="index">
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
      list: Array
    }
}
</script>

<style>

</style>
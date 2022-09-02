<template>
  <div>
    <ul>
      <h1>Film</h1>
      <li v-for="(film, index) in f_list" :key="index">
        {{film.title}} -
        {{film.original_title}} -
        {{film.original_lenguage}} -
        {{film.vote_avarage}}
      </li>
    </ul>
    <ul>
      <h1>Tv</h1>
      <li v-for="(tv, index) in s_list" :key="index">
        {{tv.name}} -
        {{tv.original_name}} -
        {{tv.original_lenguage}} -
        {{tv.vote_avarage}}
      </li>

    </ul>

  </div>
</template>

<script>
export default {
    name:"MyMain",
    props: {
      f_list: Array,
      s_list: Array
    },
    
}
</script>

<style lang="scss">

</style>
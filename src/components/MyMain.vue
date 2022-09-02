<template>
  <div>
    <section>
      <h1>Film</h1>
      <li v-for="(film, index) in f_list" :key="index">
        <img :src=" 'https://image.tmdb.org/t/p/w300' + film.poster_path " :alt="'poster' + film.title "/>
        {{film.title}} -
        {{film.original_title}} -
        {{film.original_lenguage}} -
        {{film.vote_avarage}}
      </li>
    </section>
    <sectioon>
      <h1>Tv</h1>
      <li v-for="(tv, index) in s_list" :key="index">
        <img :src=" 'https://image.tmdb.org/t/p/w300' + tv.poster_path " :alt="'poster' + tv.title " />
        {{tv.name}} -
        {{tv.original_name}} -
        {{tv.original_lenguage}} -
        {{tv.vote_avarage}}
      </li>

    </sectioon>

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
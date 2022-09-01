<template>
  <div>
    <ul>
      <li>Titolo - lingua - voto</li>
      <li v-for="(item,index) in list" :key="index">
        {{item.title}} -
        {{item.originl_title}} -
        {{item.original_lenguage}} -
        {{item.vote_avarage}}
      </li>

    </ul>

  </div>
</template>

<script>
export default {
    name:"MyMain",
    props:{
      list: Array
    }
}
</script>

<style>

</style>
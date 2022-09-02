<template>
  <div>
     <!--flag  -->
     <ul>
        <li v-for="(film, index) in list" :key="index">
            {{film.original_lenguage}}
        </li>
     </ul>
  </div>
</template>

<script>
export default {
    methods:{
        }


}
</script>

<style>

</style>
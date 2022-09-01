<template>
  <div id="app">
    <MyHeader @search="textToSearch"/>
    <MyMain :list="list"/>
  </div>
</template>

<script>


import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },

  data() {
    return {
      apiUrl:'https://api.themoviedb.org/3',
      apiKey:'24b248d3ec557ff42f3aac3b5261990e',
      lenguage: 'it-IT',
      list:[]
    }
  },


  methods: {
    textToSearch(textSearced) {
      axios.get(this.apiUrl + '/search/movie?api_key=' + this.apiKey + '&language='+ this.language + '&query=' + textSearced)
      .then(res => {
        this.list = res.data.results;
      })
      // .catch(err => {
      //   console.log(err);
      // })

    },
  }
}
</script>

<style lang="scss">

// rest rules
// * {
//   padding: 0;
//   margin: 0;
//   box-sizing: border-box;
//   font-family: sans-serif;
// }



</style>

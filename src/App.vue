<template>
  <div id="app">
    <MyHeader @search="textToSearch"/>
    <MyMain :f_list="f_list" :s_list="s_list"/>
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
      f_list:[],
      s_list:[]
    }
  },


  methods: {
    textToSearch(textSearced) {
      const paramsObj = {
          params: {
            api_key: this.apiKey,
            language: this.language,
            query: textSearced
          }
        };
      this.getMovies(paramsObj);
      this.getSeries(paramsObj);
    },
    getMovies(paramsObj) {
        axios.get(this.apiUrl + '/search/movie', paramsObj)
        .then(res => {
          this.f_list = res.data.results;
        })
        .catch(err => {
          console.log(err);
        })
    },
    geSeries(paramsObj) {
        axios.get(this.apiUrl + '/search/tv', paramsObj )
        .then(res => {
          this.s_list = res.data.results;
        })
        .catch(err => {
        console.log(err);
        })
      }
  }
}
</script>

<style lang="scss">

rest rules
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}



</style>

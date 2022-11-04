<template lang="fr">
    <div id="cards">
        <BaseCard v-for="(country,i) in countries" :key="i" :country="country"/>
    </div>
</template>
<script>
import axios from 'axios'
import BaseCard from '@/components/BaseComponents/BaseCard.vue'
export default {
  name :"AboutView",
  components : {BaseCard},
  data() {
    return {
      countries : Object,
      url : "https://restcountries.com/v3.1/all"
    }
  },
  created() {
    axios
    .get(this.url)
    .then((response)=>{this.countries = response.data; console.log(this.countries);})
    .catch(error => console.log(error))
  }
}
</script>
<style>
    #cards{
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr ;
        display : grid;
        
    }
</style>
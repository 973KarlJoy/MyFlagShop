<template lang="fr">
    <div id="cards">
        <BaseCard v-for="(country,i) in countries" 
        :key="i" :country="country" :count ="this.count" :less="downCount" :more ="upCount" />
    </div>
</template>
<script>
import axios from 'axios'
import BaseCard from '@/components/BaseComponents/BaseCard.vue'
export default {
  components : {BaseCard},
  data() {
    return {
      countries : Object,
      url : "https://restcountries.com/v3.1/all",
      count : 0,
    }
  },
  created() {
    axios
    .get(this.url)
    .then((response)=>{this.countries = response.data; console.log(this.countries);})
    .catch(error => console.log(error))
  },
  methods() {
    return {
      upCount() {
        this.count ++
      },
      downCount(){
        if(this.count >0){
          this.count--;console.log(this.count)
        }
      }
    }

  }
}
</script>
<style>
    #cards{
        grid-template-columns: 1fr 1fr 1fr 1fr ;
        display : grid;
        
    }
</style>
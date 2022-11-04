<template>
  <div class="about">
    <h1>This is an about page</h1>
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
<template lang="fr" >
    <img :src ="this.country.flags.png" :alt ="this.country.translations.fr"/>
    <h4>{{this.country.translations.fr}}</h4>
    <p>Ce pays situé en {{this.country.region}}</p>
    <div id = "PetitsBouttons">
        <button><p>-</p></button>
        <button><p>+</p></button>
    </div>
</template>
<script>
export default {
    name: "BaseCard", 
    props: {
        country : Object
    }
    
}
</script>
<style lang="">
    
</style>
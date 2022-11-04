<template lang="fr" >
    <section>
        <img :src ="this.country.flags.png" :alt ="this.country.translations.fr"/>
        <h4>{{this.country.translations.fr}}</h4>
        <p>Ce pays situé en {{this.country.region}}</p>
        <div id = "PetitsBouttons">
            <button><p>-</p></button>
            <button><p>+</p></button>
        </div>

    </section>
    
</template>
<script>
export default {
    name: "BaseCard", 
    props: {
        country : Object
    }
    
}
</script>
<style>
    section {
        margin : solid  2px black;
        border: 10px;
        padding: 20px;
        height: fit-content;
        width: fit-content;
        padding-bottom: 18px;
        display : grid;
        

    }
    section:hover{
        transform: scale(1.01);
        box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
    }
    
</style>
<template lang="fr" >
    <section>
        <div>
            <img :src ="this.country.flags.png" :alt ="this.country.translations.fr"/>
            <h4>{{this.country.translations.fr}}</h4>
            <p id ="descriptionPreview">Ce pays situé en {{this.country.region}} ...</p>
            <div id = "PetitsBouttons">
                <button @click ="less"><p>-</p></button>
                <button><p>{{this.count}}</p></button>
                <button><p>+</p></button>
            </div>
<!--revoir vidéos flexbox et grid -->
        </div>
    </section>            
    
</template>
<script>
export default {
    name: "BaseCard", 
    props: {
        country : Object,
        count : {
            type : Number,
        },
        less : {type : Function},
        more : {type : Function}
        
    },


    
}
</script>
<style>
    section {
        margin : solid  2px black;
        
        padding: 20px;
        height: max-content;
        width: fit-content;
        padding-bottom: 18px;
        display : grid;


    }
    section:hover{
        transform: scale(1.01);
        box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
    }
    section > div {
        
    }
    #PetitsBouttons{border :2px;}

    
</style>
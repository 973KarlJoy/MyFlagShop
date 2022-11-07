<template>
    <button><router-link :to="to">{{label}}</router-link></button> 
</template>
<script>
export default {
    name: "BaseButton",
    props :{
        to : {
            type : String,
            default : "/"},
        label : {
            type : String,
            required : true
        }
    }
    
}
</script>
<style scoped>
   button {
    width: fit-content;
    height: fit-content;
    color: rgb(0, 0, 206);
    border: 2px blue;
    margin : 10px
   } 
</style>
<template lang="fr">
    <div>
        <BaseInput label="Username" v-model ="event.title" type="text" />
        <BaseInput label ="password" v-model ="event.password" type ="password"/>
    </div>  
    <base-button/>


</template>
<script>
import BaseInput from '@/components/BaseComponents/BaseInput.vue';
import BaseButton from '@/components/BaseComponents/BaseButton.vue';
export default {
    name : "LoginView",
    components :{BaseInput, BaseButton},
    data(){
        return {
            event :{
                title :"",
                password :"",
            }
        }
    }
}
</script>
<style lang="">
    
</style>
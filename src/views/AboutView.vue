<template>
  <div class="about">
    <h1>This is an about page</h1>
    <AdvancedFlagCards/>
    
  </div>
</template>
<script>
import AdvancedFlagCards from '@/components/AdvancedComponents/AdvancedFlagCards.vue';
export default{
  name : "AboutView",
  components:{AdvancedFlagCards}
}

</script>
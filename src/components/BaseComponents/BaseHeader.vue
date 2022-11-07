<template lang="fr">
     <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/store">Store</router-link> |
    <router-link to ="/login">Login</router-link>
  </nav>
  <router-view/>
</template>
<script>
export default {
    name:"BaseHeader",
}
</script>
<style >   
</style>
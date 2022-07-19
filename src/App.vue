<template>
  <section>
    <friendNav></friendNav>
    <friendForm></friendForm>
    <friendCard></friendCard>
  </section>
</template>

<script>
import friendCard from './components/friend-card.vue';
import friendNav from './components/nav-card.vue';
import friendForm from './components/form-card.vue';
import 'bootstrap';
import 'bootstrap/dist/css/bootstrap.min.css';
export default {
 components:{
  friendCard,
  friendNav,
  friendForm,
 } 
}
</script>

<style>
#app {
  text-align: center;
}
</style>

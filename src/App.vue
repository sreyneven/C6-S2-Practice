<template>
  <section>
    <friendNav></friendNav>
    <friendForm @users = "addUser"></friendForm>
    <friendCard v-for:="user in users" :key = "user.id" :friend = "user"></friendCard>
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
 } ,
 data() {
  return {
    users: [{firstname: "sreyne", lastname: "ven", comment: "Ugly girl"}, ],
  }
 },
 methods: {
    addUser(firstname, lastname, comment) {
      this.users.push({firstname: firstname, lastname: lastname, comment: comment})
    }
  }
}
</script>

<style>
#app {
  text-align: center;
}
</style>

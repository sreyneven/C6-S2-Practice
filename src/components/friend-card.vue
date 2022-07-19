<template>
    <section v-for="friend of friends" :key="friend.id" class="container col-3 p-2 ">
        <div class="card shadow p-3 mb-2 bg-body rounded">
            <h3>{{friend.firstname}} {{friend.lastname}}</h3>
            <p>{{friend.comment}}</p>
        </div>
    </section>
</template>
<script>
    export default{
        data() {
            return {
                friends: [
                    {id: 1, firstname:"SreyNe",lastname:"Ven", comment:"Good lady"},
                    {id: 2, firstname:"Theavy",lastname:"Ven", comment:"Good lady"},
                    {id: 3, firstname:"Phandy ",lastname:"Ven", comment:"Best girl"},
                ]
            }
        }
    }
</script>
<style scoped>

</style>

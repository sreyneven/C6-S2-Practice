<template>
    <section class="container col-6 p-2 ">
        <div class="card shadow p-3 mb-2 bg-body rounded">
            <h3>{{friend.firstname}} {{friend.lastname}}</h3>
            <p>{{friend.comment}}</p>
        </div>
    </section>
</template>
<script>
    export default{
        props:['friend']
    }
    
</script>
<style scoped>
    .card {
        border-top: 5px solid
         red;
    }
</style>

<template>
<div class="container col-6 mt-5 ">
    <form class="card p-3 shadow p-3 mb-2 bg-body rounded mb-3 rounded" @submit.prevent = "add_user">
        <div class="form-group mt-4">
            <input type="text" class="form-control" placeholder="First name" v-model="firstname">
        </div> 
        <div class="form-group mt-4">
            <input type="text" class="form-control" placeholder="Last name" v-model="lastname">
        </div> 
        <div class="form-group mt-4">
            <input type="text" class="form-control" placeholder="Comment" v-model="comment">
        </div> 
        <div class="form-group mt-5">
            <button class="btn btn-danger btn-block form-control">ADD</button>
        </div> 
    </form>
</div>
</template>
<script>
export default{
    emits: ["users"],
    data() {
        return {
            firstname: "",
            lastname: "",
            comment: "",
        }
    },
    methods: {
        add_user() {
            if(this.firstname != "" && this.lastname != "" && this.comment != "" ){
                this.$emit("users", this.firstname, this.lastname, this.comment);
            }
                this.firstname = "";
                this.lastname = "";
                this.comment = "";
            
        }
    }
}
</script>
<style scoped>
    .card {
        border-top: 5px solid red;
    }
</style>

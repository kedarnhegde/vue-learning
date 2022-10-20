<template>
  <div class="container mt-3">
    <div class="row">
        <div class="col-lg-6">
            <div class="card shadow-lg">
                <div class="card-header bg-success text-white">
                    <p class="h3 fw-bolder">Register Here</p>
                </div>
                <div class="card-body bg-light">
                    <form @submit.prevent="register()">
                        <div class="mb-2">
                            <input v-model="user.name" type="text" class="form-control" placeholder="Name">
                        </div>
                        <div class="mb-2">
                            <input v-model="user.email" type="email" class="form-control" placeholder="Email">
                        </div>
                        <div class="mb-2">
                            <input v-model="user.password" type="password" class="form-control" placeholder="Password">
                        </div>
                        <div class="mb-2">
                            <input value="Register" class="btn btn-success" type="submit">
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'RegisterComponent',
    data: function() {
        return {
            user : {
                name: '',
                email: '',
                password: ''
            }
        }
    },
    methods: {
        register: function() {
            console.log(this.user);
            this.user.name = '';
            this.user.email = '';
            this.user.password = '';
        }
    }
}
</script>

<style>

</style>
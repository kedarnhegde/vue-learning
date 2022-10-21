<template>
  <div class="container mt-3">
    <div class="row">
        <div class="col-md-6">
            <div class="card shadow-lg">
                <div class="card-body ">
                    <div v-if="isLoggedIn">
                        <p class="h3 fw-bolder text-success">
                            Welcome User
                        </p>
                        <p class="fw-bold">
                            This is the Logged In Card. <br /> Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione nemo corrupti quod enim illum quasi! Officia maxime ipsa obcaecati necessitatibus nemo voluptas explicabo praesentium, recusandae aliquam debitis, consectetur rem laborum!
                        </p>
                    </div>
                    <div v-else>
                        <p class="h3 fw-bolder text-danger">
                            Thank You!
                        </p>
                        <p class="fw-bold">
                            This is the Logged Out Card. <br /> Lorem ipsum pound sit amet consectetur adipisicing elit. Ratione nemo corrupti quod enim illum quasi! Officia maxime ipsa obcaecati necessitatibus nemo voluptas explicabo praesentium, recusandae aliquam debitis, consectetur rem laborum!
                        </p>
                    </div>
                    <div>
                        <button v-if="!isLoggedIn" class="btn btn-success m-1" @click="login">Login</button>
                        <button v-else class="btn btn-danger m-1" @click="logout">Logout</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "AuthUser",
    data: function () {
        return {
            isLoggedIn: false
        };
    },
    methods: {
        login: function () {
            this.isLoggedIn = true;
        },
        logout: function () {
            this.isLoggedIn = false;
        }
    }
};
</script>

<style>

</style>
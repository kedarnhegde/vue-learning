<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col">
                <p class="h3 fw-bolder text-success">User List (Fetch From Axios)</p>
            </div>
        </div>
        <div v-if="loading">
            <Spinner />
        </div>
        <div v-if="errorMessage">
            <p class="fw-bolder text-danger">
                {{errorMessage}}
            </p>
        </div>
        <div v-if="!loading && users.length > 0" class="row">
            <div class="col">
                <table class="table table-hover text-center table-striped">
                    <thead class="bg-dark text-white">
                        <tr>
                            <th>Sl No.</th>
                            <th>Name</th>
                            <th>Email</th>
                            <th>Company</th>
                            <th>Website</th>
                            <th>Location</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="user in users" :key="user.id">
                            <td>{{user.id}}</td>
                            <td>{{user.name}}</td>
                            <td>{{user.email}}</td>
                            <td>{{user.company.name}}</td>
                            <td>{{user.website}}</td>
                            <td>{{user.address.city}}</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
import { UserService } from '@/services/UserService2';
import Spinner from '@/components/Spinner.vue';
export default {
    name: "UserList2",
    components: {Spinner},
    data: function() {
        return {
            loading: false,
            users: [],
            errorMessage: null
        };
    },
    created: async function () {
        try {
            this.loading = true;
            let response = await UserService.getAllUsers();
            this.loading = false;
            this.users = response.data;
        } catch (error) {
            this.loading = false;
            this.errorMessage = error;
        }
    }
}
</script>

<style>

</style>
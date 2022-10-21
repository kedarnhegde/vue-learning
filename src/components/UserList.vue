<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col">
                <p class="h3 fw-bolder text-success">User List</p>
            </div>
        </div>
        <div class="row">
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
import { UserService } from '@/services/UserService';
export default {
    name: "UserList",
    data: function() {
        return {
            users: UserService.getAllUsers()
        }
    }
}
</script>

<style>

</style>
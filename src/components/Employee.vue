<template>
    <div class="container mt-3">
        <h3>Employee</h3>
        <ul class="list-group">
            <li class="list-group-item">Employee Name:  {{this.employee.name}}</li>
            <li class="list-group-item">Employee Age: {{this.employee.age}}</li>
            <li class="list-group-item">Employee Designtion: {{this.employee.desig}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "EmployeeComponent",
    data: function () {
        return {
            employee: {
                name: 'Hegde Kedar',
                age: 18,
                desig: 'Vue Developer'
            }
        }
    }
};
</script>

<style scoped>

</style>
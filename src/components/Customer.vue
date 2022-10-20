<template>
    <div class="container mt-3">
        <h2>Customer Details: </h2>
        <ul class="list-group">
            <li class="list-group-item">Customer Name:  {{name}}</li>
            <li class="list-group-item">Customer Age: {{age}}</li>
            <li class="list-group-item">Customer Designtion: {{desig}}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "CustomerComponent",
        props: {
            name: {type: String, required: true},
            age: {type: String, required: true},
            desig: {type: String, required: true}
        }
    };
</script>

<style scoped>

</style>
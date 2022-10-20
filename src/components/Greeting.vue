<template>
  <div class="container mt-3">
    <div class="row">
        <div class="col">
            <div class="card shadow-lg">
                <div class="card-body">
                    <p class="h3">Hello, <span class="fw-bolder"> <i>{{this.msg}}</i></span></p>
                    <button  @click="greet('Good Morning')" class="btn btn-success m-1">Good Morning</button>
                    <button @click="greet('Good Afternoon')" class="btn btn-warning m-1">Good Afternoon</button>
                    <button @click="greet('Good Evening')" class="btn btn-danger m-1">Good Evening</button>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'GreetingComponent',
    data: function() {
        return {
            msg: ""
        };
    },
    methods: {
        greet: function(value) {
            this.msg = value;
        }
    }
}
</script>

<style>

</style>
<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col-md-4">
                <h3>Counter : </h3>
                <div class="card">
                    <div class="card-body shadow-lg">
                        <p class="h3 display-12">Count: {{this.count}}</p>
                        <button  @click="incr" class="btn btn-success m-1">+</button>
                        <button @click="decr" class="btn btn-danger m-1">-</button>
                        <button @click="reset" class="btn btn-warning m-1">Reset</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CounterComponent",
    data: function () {
        return {
            count: 0
        }
    },
    methods : {
        incr : function () {
            this.count += 1;
        },
        decr : function () {
            this.count -= 1;
        },
        reset: function () {
            this.count = 0;
        }
    }
};
</script>

<style scoped>

</style>
<template>
  <div class="container mt-3">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">App component</p>
          <p class="fst-italic">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam veritatis sequi sunt placeat exercitationem. Et debitis esse consequuntur necessitatibus sit libero molestiae, iste dolorum tenetur quisquam architecto error? Quos, minima.</p>
        </div>
      </div>
    </div>

  <Customer name = "Kedar Hegde" age = "22" desig = "Software Engineer"/>
  <Employee />
  </div>
</template>

<script>
  import Customer from '@/components/Customer.vue';
  import Employee from '@/components/Employee.vue'
  export default {
    name: "App",
    components: {
      Customer,
      Employee
    }
  };
</script>

<style>
  @import "./styles.css";
</style>




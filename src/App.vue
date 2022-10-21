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

  <AuthUser />
  <Customer name = "Kedar Hegde" age = "22" desig = "Software Engineer"/>
  <Employee />
  <Counter />
  <Greeting />
  <Register />
  <UserList />
  <UserList2 />
  </div>
</template>

<script>
  import Customer from '@/components/Customer.vue';
  import Employee from '@/components/Employee.vue';
  import Counter from '@/components/Counter.vue';
  import Greeting from '@/components/Greeting.vue';
  import Register from '@/components/Register.vue';
  import AuthUser from '@/components/AuthUser.vue';
  import UserList from '@/components/UserList.vue';
  import UserList2 from '@/components/UserList2.vue';

  export default {
    name: "App",
    components: {
      Customer,
      Employee,
      Counter,
      Greeting,
      Register,
      AuthUser,
      UserList,
      UserList2
    }
  };
</script>

<style>
  @import "./styles.css";
</style>




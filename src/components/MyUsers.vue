<template>
    <div class="container">
    <h3>Users:</h3>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Id</th>
          <th scope="col">Name</th>
          <th scope="col">Email</th>
          <th scope="col">City</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in myusers" v-bind:key="user.id"> 
          <th scope="row">{{user.id}}</th>
          <td>{{user.name}}</td>
          <td>{{user.email}}</td>
          <td>{{user.address.city}}</td>
        </tr>
      </tbody>
    </table> 
  </div> 
</template>


<script>
    import axios from 'axios';

    export default{
        name: 'MyUsers',
        data(){
            return {
                myusers: null,
            };
        },
        created: function() {
            axios
                .get('https://jsonplaceholder.typicode.com/users/')
                .then(res => {
          this.myusers = res.data;
            })
        }
    }
</script>

<styles>
</styles>
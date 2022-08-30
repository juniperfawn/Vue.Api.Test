<template>
    <div id = "app">
        <my-users />
    </div>
</template>

<script>
import MyUsers from './components/MyUsers.vue';

export default {
  name: 'app',
  components: {
    MyUsers,
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

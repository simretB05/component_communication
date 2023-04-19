<template>
  <div id="app">
  <small-user-profile-vue   v-for="(user, i) in users" :key="i" :user="users[i]">
    
  </small-user-profile-vue>
  </div>
</template>

<script>
import SmallUserProfileVue from './components/SmallUserProfile.vue';
export default {
  name: 'App',
  components: {
    SmallUserProfileVue
  },
  data() {
    return {
      users: [{
        name: `lula`,
        age: 29,
        is_premium: true,
        id: 101,
        
    }]
    }
  },
}
</script>

<style>
*{
  margin:0;
  padding:0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

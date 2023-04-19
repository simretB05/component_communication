<template>
  <div id="app">
    <h1 class="user_title">{{ usersName }}</h1>
  <small-user-profile-vue      @user_clicked="show_user"  v-for="(user, i) in users" :key="i" :user="users[i]">

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
  data(){
    
    return {
      usersName:'',
      users: [{
        name: `lula`,
        age: 29,
        is_premium: false,
        id: 101,
        
    }]
    }
  },
  methods: {
    show_user(name){
        this.usersName=name
    }
  }
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

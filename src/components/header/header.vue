<template>
  <header id="header">
    <div class="logo">
      <img src="data:image/png;base64,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">
      <router-link to="/">
      Vue 2 - Auth Module</router-link>
    </div>
    <nav>
      <ul>
        <li v-if="!auth">
          <router-link to="/signup">
          <i class="fas fa-user-plus"></i> Sign Up</router-link>
        </li>
        <li v-if="!auth">
          <router-link to="/signin">
          <i class="fas fa-sign-in-alt"></i> Sign In</router-link>
        </li>
        <li v-if="auth">
          <router-link to="/dashboard">
          <i class="fas fa-tachometer-alt"></i>
          Dashboard</router-link>
        </li>
        <li v-if="auth">
          <button @click="onLogout" class="logout">Logout</button>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
  export default {
    computed: {
      auth () {
        return this.$store.getters.isAuthenticated
      }
    },
    methods: {
      onLogout () {
        this.$store.dispatch('logout')
      }
    }  
  }
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css?family=Clicker+Script');

  #header {
    height: 56px;
    display: flex;
    flex-flow: row;
    justify-content: space-between;
    align-items: center;
    background-color: #521751;
    padding: 0 20px;
    font-family: 'Clicker Script', cursive;
    font-size: 22px;
  }

  .logo {
    font-weight: bold;
    color: white;
    display: flex;
    align-items: center;
  }

  .logo img {
    margin: 10px;
  }

  .logo a {
    text-decoration: none;
    color: white;
  }

  nav {
    height: 100%;
  }

  ul {
    list-style: none;
    margin: 0;
    padding: 0;
    height: 100%;
    display: flex;
    flex-flow: row;
    align-items: center;
  }

  li {
    margin: 0 16px;
  }

  li a {
    text-decoration: none;
    color: white;

  }

  li a:hover,
  li a:active,
  li a.router-link-active {
    color: #fa923f;
  }

  .logout {
    background: transparent;
    border: none;
    cursor: pointer;
    font: inherit;
    color: #fff;
  }
</style>
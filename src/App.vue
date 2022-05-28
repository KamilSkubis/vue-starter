<template>
  <div id="app">
    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <div v-if="!loggedIn">
      <label id="switch"
        >Zaloguj się e-mailem
        <input type="text" v-model="email" />
        <button @click="logMeIn()">Wchodzę</button></label
      >
    </div>
    <div v-else>
      <h2>Witaj {{ email }}</h2>
      <a @click="logOut()"> Wyloguj </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      loggedIn: false,
    };
  },
  methods: {
    logMeIn() {
      this.loggedIn = true;
    },
    logOut() {
      this.loggedIn = false;
      this.email = "";
    },
  },
};
</script>

<style>
#red {
  color: red;
}
</style>

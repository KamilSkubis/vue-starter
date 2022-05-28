<template>
  <div id="app">
    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <div v-if="!authenticatedUserName">
      <login-form @login="logMeIn($event)" button-label="Wejdź"></login-form>
    </div>
    <div v-else>
      <log-out-button @logout=logOut($event) :email="authenticatedUserName"></log-out-button>
    </div>
  </div>
</template>

<script>
import "milligram";
import LoginForm from "./LoginForm.vue";
import LogOutButton from './LogOutButton.vue';

export default {
  components: { LoginForm, LogOutButton },
  data() {
    return {
      authenticatedUserName: "",
    };
  },
  methods: {
    logOut() {
      this.authenticatedUserName = "";
    },
    logMeIn(username) {
      this.authenticatedUserName = username;
    },
  },
};
</script>

<style>
#red {
  color: red;
}
</style>

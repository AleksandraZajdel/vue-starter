<template>
  <div>
    <h1>Witaj w systemie zapisow na zajecia</h1>
    <div v-if="authenticatedEmail != ''">
      <h4>Jestes zalogowany jako {{authenticatedEmail}}</h4>
      <a @click="logMeOut()">Wyloguj</a>
      </div>
  <div v-else>
    Wpisz login:
    <input type="text" v-model="email">
    <button @click="logMeIn()">Wchodze</button>
  </div>
  </div>
</template>
<script>
import "milligram";

export default {
data() {
  return {
    email: '',
    authenticatedEmail: ''
  };
},
methods: {
  logMeIn() {
    this.authenticatedEmail = this.email;
  }
},
  logMeOut() {
    this.authenticatedEmail = '';
    this.email = ';'
  }
};
</script>

<style>

</style>

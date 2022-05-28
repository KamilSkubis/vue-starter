<template>
  <div id="app">
    <h1 >Wpisałeś {{email}}</h1>
    <input type="text" v-model="email" >
    <div v-if="email.length < 10">Ale masz krótki adres!</div>
    <div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
    <div v-else id=red >Twój adres e-mail jest stanowczo za długi.</div>
    
  </div>
</template>

<script>
export default{



data() {
  return {
    email: ''
  };
}
} 

</script>

<style>

#red {
  color: red;
}
</style>

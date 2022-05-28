<template>
  <div id="app">
    <h1>Wpisałeś {{email}}</h1>
    <input type="text" v-model="email" >

    
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

</style>

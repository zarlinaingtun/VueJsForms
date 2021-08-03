<template>
   <SignUp/>
</template>

<script>
import SignUp from './components/SignUp.vue';

export default {
     components:{
       SignUp
     }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: hsl(210, 29%, 24%);
  margin-top: 60px;
}
body{
  font-family: sans-serif;
  min-height: 100vh;
  background: linear-gradient(rgb(68, 224, 245),pink);

  display: flex;
  justify-content: center;
  align-items: center;

  margin:0;
  
}
</style>

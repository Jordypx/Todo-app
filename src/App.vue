<template>
<div class="app" :class="(mode === 'light') ? 'light' : 'dark'">

  <Header :mode='mode' @toggle="toggle" />

  <TodoList :mode='mode'/>

</div>

</template>

<script>
import Header from "./components/Header.vue";
import TodoList from "./components/TodoList.vue";


export default {
  name: 'App',
  components: {
    Header,
    TodoList
  },

   data(){
    return{
      mode: 'light',
    }
  },

   methods:{
    toggle(){
      if(this.mode === "dark"){
        this.mode = "light"
      }else{
        this.mode = "dark"
      }
    },
    
  },
}
</script>

<style>

* {
  box-sizing: border-box;
  font-family: 'Josefin Sans' , sans-serif;
}
body{
  padding:0;
  margin:0;
  max-height: 100vh;
}
#app{
  width: 100%;
  min-height: 100vh;
  transition: background 0.3s ease-in-out;
  background-color: #161722;
  font-size: 18px;
}
.dark{
  color: #FFFFFF;
}
.light{
  background-color: #E4E5F1;
  min-height: 100vh;
}

</style>

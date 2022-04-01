<template>
<nav>
   <div class="main">
      <div class="container">
         <h1>TODO</h1>
         <i  @click="$emit('toggle')" v-if=" mode === 'dark'"><img src="../assets/icon-sun.svg" alt=""></i>
         <i @click="$emit('toggle')" v-else><img src="../assets/icon-moon.svg" alt=""></i>
      </div>
   </div>
</nav>
   
</template>



<script>
export default {
   name: "Header",
    props:['mode'],
}


</script>


<style scoped>
nav{
    background-image:url(../assets/bg-desktop-dark.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 35vh;
    width: 100%;
    transition: background 0.3s ease-in-out;
}

.main{
    color: #FFFFFF;
    width: 100%;
    align-items: center;
    margin: 0 auto;
}

.container{
    display: flex;
    justify-content: space-around;
    margin: 0 auto;
    text-align: center;
    width: 100%;
    gap: 12rem;
}

 @media screen and (min-width: 375px) {
   .container {
    width: 100%;
    gap: 17rem;
   }
} 

h1, i{
    margin-top: 5rem;
}
h1{
    letter-spacing: 10px;
    font-size: 2.3rem;
}

i {
   cursor: pointer;
}

@media screen and (min-width: 880px){
    nav{
        background-position: 0 -120px;
    }
    .container{
        width: 70%;
    }
}

.light nav{
    background-image:url(../assets/bg-desktop-light.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 35vh;
    width: 100%;
}
</style>
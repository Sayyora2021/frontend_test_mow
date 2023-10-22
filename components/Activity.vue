<template>
<div class="body"> 
    <h1>Rechercher par activité</h1>
    <div  class="boxes">
    <div class="card"><font-awesome-icon :icon="['fas', 'skiing']" class="icon" /></div>
    <div class="card"><font-awesome-icon :icon="['fas', 'swimmer']" class="icon"/></div>
     <div class="card"> <font-awesome-icon :icon="['fas', 'hiking']" class="icon"/></div>
     <div class="card"> <font-awesome-icon :icon="['fas', 'parachute-box']"  class="icon"/></div>
     <div class="card"><font-awesome-icon :icon="['fas', 'volleyball-ball']" class="icon"/></div>
    </div>

</div>

</template>
<script>

export default {
   
}
</script>

<style scoped>
h1{
    font-family: 'Railway' , sans-serif;
   padding:50px;
  
}
.card {
  width: 190px;
  height: 190px;
  border-radius: 30px;
  background: #e0e0e0;
  box-shadow: 15px 15px 30px #bebebe;
             /* -15px -15px 30px #ffffff; */
             border: 5px solid transparent;
    transition: border-color 0.3s; 
}
.card:hover{
    border-color:rgb(8, 188, 8);
    box-shadow: 10px 10px 10px rgb(187, 238, 187);
}
.icon{
    width:50px;
    height:50px;
    color:rgb(8, 188, 8);
    padding:60px;
}
.boxes{
    display:flex;
    justify-content:space-between;
    flex-wrap:wrap;
     margin:30px;
     gap:10px;
}
.body{
    background-color: #e6e3e3;
    height:auto;
    padding:20px;
   
}

</style>
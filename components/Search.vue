<template>
<div class="input-container">
     
    <font-awesome-icon :icon="['fas', 'search']" class="search-icon" />    
    <input placeholder= "Ville, pays" type="text" name="text" class = "input">
    <button class="buttonSearch">Rechercher</button>
    
</div>
</template>
<script>

export default {
   
}
</script>
<style scoped>
.input-container {
  display: flex;
  justify-content: center; 
  padding:50px;
  position:relative;
}

input{
     width: 80%;
    height: 55px;
  padding: 18px;
  padding-left:55px;
   border-radius: 12px 0 0 12px;
  border: 1.5px  solid grey;
  outline: none;
  transition: all 0.3s cubic-bezier(0.19, 1, 0.22, 1);
  box-shadow: 0px 0px 20px -18px;
  margin-left:5px;
  
 }
.input{
    font-size:18px;
    color:black;
    font-family: 'Railway-Bold.ttf';
    font-weight: bold;;
}

.search-icon{
    color: rgb(152, 44, 5);
    font-size: 40px;
  padding:20px 10px 0px 10px;
  position:absolute;
  left:6%;
  right:2%;
  top:45%;
  transform: translateY(-50%);
  width:40px;
  z-index: 1;
  
}

.buttonSearch {
  height:93px;
  width: 120px;
  cursor: pointer;
  font-weight: bold;
  font-family: 'Railway-Bold.ttf';
  font-size:18px;
  border-radius: 0 10px 10px 0;
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: lightgrey;
     border: 1.5px  solid grey;
  
}
@media (max-width: 770px) {
 .search-icon {
    left:10%;
    
  }
}

</style>
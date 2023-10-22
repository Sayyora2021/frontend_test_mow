<template>
    <header>
<img src="@/assets/img/logo.png" alt="Le logo Loisira">
 <ul>
  <li>
   <font-awesome-icon :icon="['fas', 'book-open']" class="icon"></font-awesome-icon> Réservation
    </li>
   
    <li><font-awesome-icon :icon="['fas', 'mail-bulk']" class="icon"></font-awesome-icon>Contact</li>
</ul>
    </header>
</template>
<script>

export default {
    
}
</script>
<style scoped>
header{
    padding:20px;
}
img{
    width:calc(60% + 3vw);    
}
header{
    width:calc(60% + 3vw); 
  margin: 0 auto;
  text-align: center;
  margin-top:50px;
    
}

ul{
  display:flex; 
  color:rgb(230, 90, 39);
font-size: 36px;
justify-content: space-between;
font-family: 'Railway-ExtraBold.ttf';
list-style: none;
width:90%;
}
.icon{
    width:50px;
}
li{
    font-size: calc(15px + 2vw); 
    gap:10px;
    display:flex;
}
</style>
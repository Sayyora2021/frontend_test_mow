<template>
    <div>
        <h1>Nos coup de coeur</h1>
        <div class="cards">
<div class="container" v-for="ville in villes" :key="ville.id">
       <img :src="require(`../assets/img/${ville.cover}`)" :alt="ville.alt" class="size"/>  
       <h2>{{ ville.title }}</h2>
       <div class="line">
       <p class="city-name">{{ ville.pays }}</p>
       <div class="price">
       <p>{{ ville.prix }}</p>
       <span>{{ville.euro}}</span>
       </div>
       </div>
</div>

        </div>
    </div>
</template>
<script>
import data from '@/static/loisir.json';

export default{
    data(){
        return{
            villes:data.villes
        }
    }
}
</script>

<style scoped>
h1{
    font-family: 'Railway' , sans-serif;
   padding:50px;
  
}
.container {
  width: 350px;
  height: 235px;
  position: relative;
  border-radius: 23px 23px 0 0;
  transition: all 0.8s cubic-bezier(0.15, 0.83, 0.66, 1);
  cursor: pointer;
  background: #e0e0e0;
  box-shadow: 15px 15px 30px #bebebe;
}
.cards{
    display:flex;
    justify-content:space-between;
    flex-wrap: wrap;
    gap:20px;
    margin:30px;
}
.size{
    width:350px;
    height:150px;
    border-radius:23px 23px 0 0;
}
.line{
    display:flex;
    justify-content: space-between;
    padding:10px;
    font-family:'Railway' , sans-serif;
}
.price{
    padding-bottom:10px;
    display:flex;
    gap:5px;
    color:rgb(81, 79, 79)
}
h2{
    padding:10px
}
.city-name{
    font-size:12px;
    font-family: 'Railway' , sans-serif;
    color:grey;
}
span{
    font-weight:bold;
    color:black;
    font-family: 'Raleway-Bold' sans-serif;
}
@media (min-width: 1024px) {
  .cards {
    display:flex;
    
  }
  .container{
    width:300px;

  }
  .size{
    width:300px;
  }
}
</style>
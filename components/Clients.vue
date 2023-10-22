<template>
    <div class="body">
        <h1>Nos retours clients</h1>
        <div class="grid-container">
       <div v-for="client in clients" :key="client.id">
         <div class="left-content">
          <img :src="require(`../assets/img/${client.img}`)" :alt="client.alt" class="client-img"/> 
         </div>
         <div class="right-content">
           <h2>{{ client.nom }}</h2>
        <p class="description">"{{ client.description }}"</p>
           
  <div class="stars" v-if="client.rating">
    <svg
      v-for="(star, index) in stars(parseInt(client.rating))"
      :key="index"
      class="star"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 24 24"
      :style="{ fill: star === 'full' ? 'green' : 'transparent', width: '40px', height: '40px', stroke: 'green', strokeWidth: 2 }"
      :src="star === 'full' ? require(`../assets/img/star-solid.svg`) : require(`../assets/img/star-regular.svg`)"
      :alt="star === 'full' ? 'étoile pleine' : 'étoile vide'"
     
    >
    <path d="M12 2l2.7 6.8H20l-5.2 4.6 2.1 6.3L12 15.4 7.3 19.7l2.1-6.3L4 8.8h5.3L12 2z" />
  </svg>
  </div>
         </div>
        </div>
       </div>
      <div class="button-container">
        <button class="custom-btn btn-1"><p>Voir tous les avis</p></button>
    </div>
    </div>
</template>

<script>

import data from '@/static/loisir.json';

export default{
    data(){
        return{
            clients:data.clients
        };
    },
    methods: {
    stars(rating) {
      const starArray = [];
      for (let i = 1; i <= 5; i++) {
        starArray.push(i <= rating ? 'full' : 'empty');
      }
      return starArray;
    }
        }
    }

</script>
<style scoped>
.body{
    background-color: rgb(230, 230, 230);
    padding:40px;
    
}
.client-img{
    width:100px;
    height:100px;
    border-radius:50px;
    vertical-align: middle;
}
h1{
    font-family: 'Railway' , sans-serif;
   padding:30px;
}
.left-content {
    flex: 0 0 auto; /* Partie gauche ne doit pas grandir ou rétrécir */
    margin-right: 10px; /* Espace entre l'image et le texte */
 
}
.grid-container {
  display: grid;
  grid-template-columns: repeat(1, 1fr); 
  grid-gap: 20px;  
}
.right-content{
flex:1;
position:relative;
left:150px;
top:-90px;
width:80%;

height:50px;
}
.description{
    vertical-align:middle;
    font-family: 'Railway' , sans-serif;
    color:rgb(108, 106, 106);
}
.stars{
    color:rgb(2, 163, 2);
    width:150px;
    height:150px;
    display:flex;
}
.button-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: auto; 
    margin:80px;
}

.custom-btn {
    width: 330px;
    height: 60px;
    color: #fff;
    border-radius: 12px;
    padding: 10px 25px;
    font-family: 'Lato', sans-serif;
    font-weight: 500;
    background: transparent;
    cursor: pointer;
    transition: all 0.3s ease;
    position: relative;
    display: inline-block;
    box-shadow: inset 2px 2px 2px 0px rgba(255,255,255,.5),
    7px 7px 20px 0px rgba(0,0,0,.1),
    4px 4px 5px 0px rgba(0,0,0,.1);
    outline: none;
}

.btn-1 {
    background: rgb(5, 195, 128);
    background: linear-gradient(0deg, rgb(3, 154, 101) 0%, rgb(15, 154, 96) 100%);
    border: none;
}

.btn-1:before {
    height: 0%;
    width: 2px;
}

.btn-1:hover {
    box-shadow: 4px 4px 6px 0 rgba(255,255,255,.5),
    -4px -4px 6px 0 rgba(116, 125, 136, .5), 
    inset -4px -4px 6px 0 rgba(255,255,255,.2),
    inset 4px 4px 6px 0 rgba(0, 0, 0, .4);
}
p{
    font-family: 'Railway'; 
    font-size:22px;
    
}
@media (min-width: 1024px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr); /* Deux colonnes en mode desktop */
  }
}

</style>
<template>
    <div class="body">

<h3>Navigation</h3>
<p>Réservation</p>
<p>Contact</p>

<h3>A propos de nous</h3>
<p>Notre équipe</p>
<p>Nos conditions d'utilisations</p>
<p>Nos conditions de vente</p>
<div class="text">
<h3>Inscrivez-vous à notre newsletter</h3>
<input type="email" id="email" name="email" placeholder="Adresse Email">
</div>
<div class="logo">
    <img src="@/assets/img/tripadvisor.png" alt="L'icon de tripadvisor" class="trip-logo">
    <font-awesome-icon :icon="['fab', 'facebook-f']" class="facebook"/>
    <font-awesome-icon :icon="['fab', 'instagram']" class="social-links" />
    <font-awesome-icon :icon="['fab', 'twitter']" class="social-links"/>
</div>

<span>@2021 - Loisirama | Mine Of War Developpement template - Tous droits résérvés</span>

    </div>
</template>

<style scoped>
.body{
    margin:50px;
   
}


h3{
    color:brown;
    font-family: 'Railway', sans-serif;
   margin:30px;
}
p{
     font-family:'Railway' , sans-serif;
     color:rgb(230, 90, 39);
     font-size: 18px;
     margin:30px;
}
input{
   cursor:pointer;
   width:250px;
   height:40px;
   background:lightgray;
   border-radius:10px;
    margin-left:30px;
    padding:5px;
   border:1px solid rgba(27, 31, 35, 0.15);
   font-size:16px;
   font-family:'Railway' , sans-serif;
   
}
.logo{
    float:right;
    display:flex;
    gap:10px;
    color:brown;
    height:30px;
}
.trip-logo{
    width:30px;
    height:25px;
    background-color:brown;
}
.social-links{
    height:50px;
    width:40px;
}
.facebook{
    width:40px;
    height:40px;
}
span{
    display:flex;
    margin:50px;
    justify-content: center;
    font-family: 'Railway' , sans-serif;
    font-size:18px;
    padding:50px;
}
@media(min-width:1024px){
    .text{
        display:flex;
        justify-content: end;
    }
}
</style>
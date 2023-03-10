<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <header>
        <div class="left-header">
            <img src="../assets/img/Logo.png" alt="" id="logo">
            <h1>ApparToutou</h1>
        </div>
        <div class="search-bar">
            <input type="text" placeholder="rechercher">
        </div>
        <div class="menu">
            <RouterLink to="/"><img src="../assets/img/niche.png" alt="home" class="icon"></RouterLink>
            <RouterLink to="/connexion"><img src="../assets/img/dog.png" alt="profil" class="icon"></RouterLink>
        </div>

    </header>
</template>

<style scoped>
#logo{
    width: 100px;
    margin: 10px;
}
header{
    display: flex;
    justify-content: space-between;
    position: fixed;
    width: 100%;
    align-items: center;
    background-color: rgba(36, 30, 78, 0.9);
}
h1{
    color: #EADAA2;
    font-size: 25px;
}
.left-header{
    display: flex;
    align-items: center;
}
input{
    font-size: 15px;
    width: 250px;
}
.search-bar{
    display: inherit;
    align-items: center;
    margin: 25px;
}
.icon{
    width: 40px;
    margin: 10px;
}
.menu{
    margin-right: 25px;
}
</style>
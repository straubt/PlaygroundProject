<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<script>
export default{
    props:{
        apart:null
    }
}
</script>

<template>
    <div class="apart">
        <div class="img">
            <img :src="apart.img" alt="image">
        </div>
        <div class="description">
            <p>{{ apart.title }}</p>
            <p>Ville : {{ apart.city }}</p>
            <p>Surface : {{ apart.surface }} m²</p>
            <p>Prix : {{ apart.price }} €</p>
        </div>
    </div>
            
</template>

<style scoped>
img{
    width: 100%;
    margin: 0px;
    border-radius: inherit;
}
.img{
    margin-bottom: 2%;
    width: 100%;
    border-radius: inherit;
}
.description{
    display: flex;
    height: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    margin-bottom: 2%;
}
.apart{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: rgba(255, 208, 70, 0.6);
    border-radius: 2%;
    margin: 2%;
    width: 80%;
}
p{
    color: #B44D22;
    font-size: larger;
}
</style>
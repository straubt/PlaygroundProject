<script setup>
import HeaderItem from '../components/HeaderItem.vue'
import { RouterLink, RouterView } from 'vue-router'
import ApartmentItem from '../components/ApartmentItem.vue'
import data from '../data/homes.json'
import axios from 'axios'
</script>

<script>
export default {
  name: "HomeView",
  data(){
    return{
      AllSejours: null,
    }
  },

  mounted(){
        try {
            axios.get('https://localhost:7112/api/Sejours/GetAll').then((reponse) => {
            this.AllSejours = reponse.data;
            console.log(JSON.stringify(this.AllSejours));
            console.log(reponse.data);
        });
        } catch (error) {
            console.log(error);
        }
    },


}
</script>

<template>
  <HeaderItem></HeaderItem>
  <main>
    <div class="apartments">
      <ApartmentItem v-for="apart in data" :apart=apart></ApartmentItem>
    </div>
    <p>{{ AllSejours }}</p>
  </main>
</template>

<style scoped>
.apartments{
  display: flex;
}
</style>

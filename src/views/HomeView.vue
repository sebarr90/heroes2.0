<template>
  <v-container class="container">
    <v-row class="description">
        <h1>Desafia las expectativas de los MOBA</h1>
        <p>Epicos heroes y accion sin cesar en multples campos de batalla</p>
        <v-btn class="btn-heroes" color="orange darken-3" @click="$router.push('/HeroesView')">Ver Heroes</v-btn>
    </v-row>
  </v-container>
  <v-alert class="desp-heroes" color="purple darken-1" v-model="alert" border="start" close-label="Close Alert" variant="tonal"><span class="text-descript">!Te damos la bienvenida al Nexo¡!En este reino entre reinos, todo es posible¡ Elige entre decenas de heroes legendarios de todo el panteón de Blizzard, personaloza sus talentos y habilidades en medio del combate y lucha en una infinidad de campos de batalla que redefinen el genero. ¡Esto no es un MOBA promedio, esto es Heroes of the Storm¡</span></v-alert>
</template>

<script> 
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomeView',

  components: {
  },
});
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  width:35%;
  margin-top:100px;
  border: 3px solid gray;
}
.description {
  display:flex;
  flex-direction: column;
  color: white;
  padding: 15px;
}
.description h1, .description p {
  margin-bottom: 10px;
}
.btn-heroes {
  margin-top:10px;
  margin-bottom:10px;
  width: 25%;
  align-self: center;
}
.desp-heroes {
  margin-top: 100px;
  height: 150px;
  font-size: 20px;
}
.text-descript{
  color: whitesmoke;
  opacity: 0.8;
}
</style>
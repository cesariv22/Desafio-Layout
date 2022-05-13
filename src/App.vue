<template>
  <div>
    <div>
      <v-app-bar color="deep-purple accent-4" dense dark>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
        <v-toolbar-title>My App</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn>
          <v-text>Inicio</v-text>
        </v-btn>
        <v-btn>
          <v-text>Buscar</v-text>
        </v-btn>
        <v-btn>
          <v-text>A cerca de</v-text>
        </v-btn>
        <v-menu left bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn icon v-bind="attrs" v-on="on">
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </template>
          <v-list>
            <v-list-item v-for="n in 5" :key="n" @click="() => {}">
              <v-list-item-title>Option {{ n }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-app-bar>
    </div>

    <PictureCard />
  </div>
</template>

<script>
import PictureCard from "./components/PictureCard";
export default {
  name: "App",
  components: {
    PictureCard,
  },
  data() {
    return {
      personajes: [
        {
          id: 1,
          nombre: "Morty",
          imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
          status: "Alive",
          especie: "Human",
        },
        {
          id: 2,
          nombre: "Rick",
          imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
          status: "Alive",
          especie: "Human",
        },
        {
          id: 3,
          nombre: "Summer",
          imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
          status: "Alive",
          especie: "Human",
        },
        {
          id: 4,
          nombre: "Beth",
          imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
          status: "Alive",
          especie: "Human",
        },
        {
          id: 5,
          nombre: "Jerry",
          imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
          status: "Alive",
          especie: "Human",
        },
        {
          id: 6,
          nombre: "Abadango",
          imagen: "https://rickandmortyapi.com/api/character/avatar/6.jpeg",
          status: "Alive",
          especie: "Animal",
        },
        {
          id: 7,
          nombre: "Abradolf",
          imagen: "https://rickandmortyapi.com/api/character/avatar/7.jpeg",
          status: "Alive",
          especie: "Human",
        },
        {
          id: 8,
          nombre: "Adjudicator",
          imagen: "https://rickandmortyapi.com/api/character/avatar/8.jpeg",
          status: "unknown",
          especie: "Human",
        },
        {
          id: 9,
          nombre: "Agency",
          imagen: "https://rickandmortyapi.com/api/character/avatar/9.jpeg",
          status: "Dead",
          especie: "Human",
        },
      ],
    };
  },
};
</script>

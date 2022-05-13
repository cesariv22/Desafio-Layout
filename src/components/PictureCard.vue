<template>
  <v-container grid-list-md>
    <v-layout row wrap>
      <v-flex v-for="item in items" :key="item.id">
        <v-card>
          <v-img class="white--text align-end" height="380px" :src="item.image">
          </v-img>
          <v-card-title class="pb-0"> {{ item.name }} </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "PictureCard",

  data() {
    return {
      items: [
        {
          id: "1",
          name: "Morty Smith",
          image: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          id: "2",
          name: "Morty Smith",
          image: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          id: "3",
          name: "Summer Smith",
          image: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          id: "4",
          name: "Beth Smith",
          image: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          id: "5",
          name: "Beth Smith",
          image: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
        {
          id: "6",
          name: "Jerry Smith",
          image: "https://rickandmortyapi.com/api/character/avatar/6.jpeg",
        },
        {
          id: "7",
          name: "Abradolf",
          image: "https://rickandmortyapi.com/api/character/avatar/7.jpeg",
        },
        {
          id: "8",
          name: "Adjudicator",
          image: "https://rickandmortyapi.com/api/character/avatar/8.jpeg",
        },
        {
          id: "9",
          name: "Agency",
          image: "https://rickandmortyapi.com/api/character/avatar/9.jpeg",
        },
      ],
    };
  },

  props: {
    text: String,
  },
};
</script>
<style scoped>
body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>

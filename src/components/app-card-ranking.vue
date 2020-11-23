<template>
  <v-container
    fluid
    grid-list-md
  >
    <v-layout row wrap>
      <v-flex
        v-for="card in cards"
        :key="card.title"
        v-bind="{ [`xs${card.flex}`]: true }"
      >
        <v-card>
          <v-card-text class="text-center">
            <span class="headline" >{{card.title}}</span>
          </v-card-text>

          <v-card-actions>
            <v-btn icon>
              <v-icon>mdi-plus</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <v-btn icon v-if="card.fav" @click="card.fav = !card.fav">
              <v-icon color="yellow">mdi-bookmark</v-icon>
            </v-btn>
            <v-btn icon v-else @click="card.fav = !card.fav">
              <v-icon >mdi-bookmark</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-share</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
            <v-btn icon v-if="card.show" @click="card.show = !card.show">
              <v-icon>mdi-chevron-up</v-icon>
            </v-btn>
            <v-btn icon v-else @click="card.show = !card.show">
              <v-icon>mdi-chevron-down</v-icon>
            </v-btn>
          </v-card-actions>

          <v-card-text v-show="card.show" v-for="list in card.list" :key="list.item">
            {{list.item}}
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    name: 'AppCard',

    data: () => ({
      cards: [
        { title: 'Name Teste',
          flex: 4,
          fav: true,
          show: false,
          list: [
            {item:"nome 1"},
            { item:"nome 2"},
            {item:"nome 3"}
          ],
        },
        { title: 'Favorite Teste',
          flex: 4,
          fav: false,
          show: true,
          list: [
            {item:"favorito 1"},
            { item:"favorito 2"},
            {item:"favorito 3"}
          ],
        },
        { title: 'House Teste',
          flex: 4,
          fav: false,
          show: false,
          list: [
            {item:"casa 1"},
            { item:"casa 2"},
            {item:"casa 3"}
          ],
        },
      ],
    }),

    methods: {

    }
  }
</script>

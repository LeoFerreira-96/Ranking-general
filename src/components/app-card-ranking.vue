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
          <div height="350px"
          >
          <v-list>
            
          </v-list>
            <v-container
              fill-height
              fluid
            >
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                  <span class="headline white--text" v-text="card.title"></span>
                </v-flex>
              </v-layout>
            </v-container>
          </div>

          <v-card-actions>
            <v-btn flat color="primary">Explorar</v-btn>
            <v-spacer></v-spacer>
            <v-btn icon>
              <v-icon>mdi-bookmark</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-share</v-icon>
            </v-btn>
          </v-card-actions>
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
        { title: 'Teste', list: ["nome1", "nome2","nome3"], flex: 3 },
        { title: 'Favorite Teste', list: ["Teste1", "Teste2","Teste3"], flex: 3 },
        { title: 'Best Teste', list: ["Casa1", "Casa2","Casa3"], flex: 3 }
      ]
    })
  }
</script>

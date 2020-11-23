<template>
  <v-container>
    <v-row class="text-center">
      <h2 class="headline font-weight-bold mb-3">
        Ranking List
      </h2>
      <v-spacer></v-spacer>
      <v-dialog v-model="dialog" persistent max-width="290">
      <template v-slot:activator="{ on }">
        <v-btn text color="primary" v-on="on"><v-icon>mdi-plus</v-icon>Criar Novo</v-btn>
      </template>
      <v-card>
        <v-card-title class="headline">Criar novo Ranking</v-card-title>
        <v-card-text>
          <input>
          <input>
        </v-card-text>
        <v-card-actions>
          <v-btn color="green darken-1" text @click="dialog = false">Cancelar</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="green darken-1" text @click="dialog = false">Criar</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
    </v-row>
    <v-layout>
    <v-flex xs12>
      <AppCard />
    </v-flex>
  </v-layout>
  </v-container>

  
</template>

<script>
  import AppCard from "./app-card-ranking"

  export default {
    name: 'Content',

    components: {
      AppCard,
    },
    data() {
      return {
        dialog: false
      }
      
    },
    methods: {
      New() {
        
      }
    }
  }
</script>

<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <span class="mr-2">RANKING GENERAL</span>

      <v-spacer></v-spacer>
      
      <v-btn
        text
      >
        <span class="mr-2">Perfil</span>
        <v-icon>mdi-account</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Content/>
    </v-main>
  </v-app>
</template>

<script>
import Content from './components/Content';

export default {
  name: 'App',

  components: {
    Content,
  },

  data: () => ({
    //
  }),
};
</script>

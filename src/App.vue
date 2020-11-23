<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <span class="mr-2">Logo Ranking General</span>

      <v-spacer></v-spacer>
      
      <v-btn icon class="ma-3">
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

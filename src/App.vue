<template>
  <v-app>
    <v-main>
      <v-container fluid>
        <MyMainscreen />
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
import MyMainscreen from './components/Mainscreen.vue';

export default {
  name: 'App',

  components: {
    MyMainscreen
  },

  data: () => ({
    //
  }),
}
</script>

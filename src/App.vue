<template>
  <v-app>
    <v-content class="text-justify">
      <h1 class="display-1 py-6 font-weight-bold text-center">Funkcje w matematyce</h1>

      <WhatIsAFunction id="WhatIsAFunction" />
      <LinearFunction id="LinearFunction" />
      <SquareFunction id="SquareFunction" />
    </v-content>
  </v-app>
</template>

<script>
import WhatIsAFunction from '@/components/WhatIsAFunction'
import LinearFunction from '@/components/LinearFunction'
import SquareFunction from '@/components/SquareFunction'

export default {
  name: 'App',

  components: {
    WhatIsAFunction,
    LinearFunction,
    SquareFunction
  },

  data: () => ({
    //
  }),
};
</script>

<style>
  #app {
    background: url("./assets/paper.png");
    background-repeat: repeat;
  }
</style>

<template>
  <v-app>
    <v-content class="text-justify">
      <v-container>
        <v-row class="mx-0" align="center" justify="space-between">
          <h1 class="display-1 py-6 font-weight-bold d-inline-flex">
            <v-img src="@/assets/function.svg" :height="48" :width="50"></v-img>
            <div class="pl-1">nkcje w matematyce</div>
          </h1>
          <v-btn color="red" outlined @click="$vuetify.goTo('#About')">O stronie</v-btn>
        </v-row>
      </v-container>

      <WhatIsAFunction id="WhatIsAFunction" />
      <LinearFunction id="LinearFunction" />
      <SquareFunction id="SquareFunction" />
      <About id="About" />
    </v-content>
  </v-app>
</template>

<script>
import WhatIsAFunction from '@/components/WhatIsAFunction'
import LinearFunction from '@/components/LinearFunction'
import SquareFunction from '@/components/SquareFunction'
import About from '@/components/About'

export default {
  name: 'App',

  components: {
    WhatIsAFunction,
    LinearFunction,
    SquareFunction,
    About
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
